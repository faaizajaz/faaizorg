<template>
  <div>
    <h1 class="page-heading">
      {{ blogPost.title }}
    </h1>
    <hr>
    <Author :author="blogPost.author" :updated="formatDate(blogPost.updatedAt)" />
    <nav>
      <ul>
        <li v-for="link in blogPost.toc" :key="link.id">
          <NuxtLink :to="`#${link.id}`" :class="{ 'l1': link.depth === 2, 'l2': link.depth === 3}">
            {{ link.text }}
          </NuxtLink>
        </li>
      </ul>
    </nav>
    <PrevNext :prev="prev" :next="next" />
    <nuxt-content class="blog-post" :document="blogPost" />
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

.l2 {
  padding-left: 8px;
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
</style>
