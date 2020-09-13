<template>
  <div>
    <h1>
      {{ blogPost.title }}
    </h1>
    <p class="">
      Updated: {{ formatDate(blogPost.updatedAt) }}
    </p>
    <nuxt-content :document="blogPost" />
    <p>{{ blogPost }}</p>
  </div>
</template>

<script>
export default {
  async asyncData ({ $content, params }) {
    const blogPost = await $content('blog', params.slug).fetch()
    return { blogPost }
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

</style>
