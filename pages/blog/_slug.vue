<template>
  <div>
    <nav>
      <ul>
        <li v-for="link in blogPost.toc" :key="link.id">
          <NuxtLink :to="`#${link.id}`" :class="{ 'l1': link.depth === 2, 'l2': link.depth === 3}">
            {{ link.text }}
          </NuxtLink>
        </li>
      </ul>
    </nav>
    <Author :author="blogPost.author" />
    <PrevNext :prev="prev" :next="next" />
    <h1>
      {{ blogPost.title }}
    </h1>
    <p class="">
      Updated: {{ formatDate(blogPost.updatedAt) }}
    </p>
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
  margin: 0 auto;
  /* min-height: 100vh; */
  display: flex;
  justify-content: left;
  align-items: top;
  text-align: justify;
}

</style>
