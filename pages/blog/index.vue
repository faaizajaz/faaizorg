<template>
  <div id="blog-home-content">
    <h1 class="page-heading">
      Blog
    </h1>
    <hr>
    <p>
      This is my blog. Maybe I'll use it, maybe I won't.
    </p>
    <ul id="blog-home-list">
      <li v-for="post in allPosts" :key="post.slug">
        <NuxtLink :to="{ name: 'blog-slug', params: { slug: post.slug }}">
          <h5>{{ post.title }}</h5>
        </NuxtLink>
        <span>{{ post.description }}</span>
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

#blog-home-list {
  list-style-type: none;
  padding-left: 5px;
  padding-right: 5px;
}

#blog-home-list li a {
  color: #3399cc;
  font-weight: bold;
}

</style>
