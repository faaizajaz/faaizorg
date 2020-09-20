<template>
  <div>
    <h1 class="page-heading">
      {{ blogPost.title }}
    </h1>
    <nav>
      <div class="toc">
        <p id="toc-title">
          Table of contents:
        </p>
        <hr>
        <ul class="toc-ul">
          <li v-for="link in blogPost.toc" :key="link.id">
            <NuxtLink :to="`#${link.id}`" class="toc-link" :class="{ 'l1': link.depth === 2, 'l2': link.depth === 3}">
              {{ link.text }}
            </NuxtLink>
          </li>
        </ul>
      </div>
    </nav>
    <hr>
    <Author :author="blogPost.author" :updated="formatDate(blogPost.updatedAt)" />
    <nuxt-content class="blog-post" :document="blogPost" />
    <hr>
    <PrevNext :prev="prev" :next="next" />
  </div>
</template>

<script>
export default {
  async asyncData ({ $content, params }) {
    const blogPost = await $content('blog', params.slug).fetch()
    const [prev, next] = await $content('blog')
      .only(['title', 'slug'])
      .sortBy('createdAt', 'asc')
      .surround(params.slug)
      .fetch()
    return {
      blogPost,
      prev,
      next
    }
  },
  methods: {
    formatDate (date) {
      const options = { year: 'numeric', month: 'long', day: 'numeric' }
      return new Date(date).toLocaleDateString('en', options)
    }
  }
}
</script>

<style>
.icon.icon-link {
  background-image: url('~assets/svg/icon-hashtag.svg');
  display: inline-block;
  width: 20px;
  height: 20px;
  background-size: 20px 20px;
}

.blog-post {
  text-align: left;
}

.page-heading {
  font-family: 'Bitter', serif;
  text-align: left;
}

hr {
  border-top: 1px solid lightgrey ;
  width: 100%;
  margin-top: 0px;
  margin-bottom: 5px;
}

.toc {
  background-color: #ededed;
  display: inline-block;
  min-width: 150px;
  width: 100%;
  padding: 10px 15px;
  list-style-type: none;
  border-radius: 10px;
  margin-bottom: 13px;

}

.toc-ul {
  list-style-type: none;
  padding-left: 0px;
}

.toc-link {
  color: #3399cc;
}

.l1 {
  font-size: 20px;
  text-decoration: underline;
  text-decoration-style: single;
}

.l2 {
  padding-left: 16px;
  font-size: 16px;
  text-decoration: underline;
  text-decoration-style: dotted;
}

#toc-title {
  margin-bottom: 0px;
  font-size: 22px;
  font-weight: bold;
}

</style>
