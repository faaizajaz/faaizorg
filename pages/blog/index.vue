<template>
  <div class="blog-home-content">
    <ul>
      <li v-for="post in allPosts" :key="post.slug">
        <NuxtLink :to="{ name: 'blog-slug', params: { slug: post.slug }}">
          <h5>{{ post.title }}</h5>
          <span>by {{ post.author.name }}</span>
          <span>{{ post.description }}</span>
        </NuxtLink>
        <hr>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  async asyncData ({ $content, params }) {
    const allPosts = await $content('blog')
      .only(['title', 'description', 'img', 'slug', 'author'])
      .sortBy('createdAt', 'asc')
      .fetch()

    return {
      allPosts
    }
  }
}
</script>

<style>

</style>
