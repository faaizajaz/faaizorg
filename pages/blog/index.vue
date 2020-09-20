<template>
  <div id="blog-home-content">
    <h1 class="page-heading">
      Blog
    </h1>
    <hr>
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

<style scoped>

.page-heading {
  font-family: 'Bitter', serif;
  text-align: left;
}

hr {
  border-top: 1px solid lightgrey ;
  width: 100%;
  margin-top: 0px;
}

</style>
