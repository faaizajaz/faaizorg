<template>
  <div id="blog-body">
    <h1 class="page-heading">
      {{ blogPost.title }}
    </h1>
    <BarDivider />
    <nav>
      <div class="toc">
        <ul class="toc-ul">
          <li v-for="link in blogPost.toc" :key="link.id">
            <NuxtLink :to="`#${link.id}`" class="toc-link" :class="{ 'l1': link.depth === 2, 'l2': link.depth === 3}">
              {{ link.text }}
            </NuxtLink>
          </li>
        </ul>
      </div>
    </nav>
    <hr class="hr-lowmb">
    <Author :author="blogPost.author" :created="formatDate(blogPost.createdAt)" />
    <nuxt-content class="blog-post" :document="blogPost" />
    <hr class="hr-1px">
    <PrevNext :prev="prev" :next="next" />
  </div>
</template>

<script>
import BarDivider from '../../components/BarDivider'

export default {
  components: {
    BarDivider
  },
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
#blog-body {
  margin-bottom:250px;
}

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

@media screen and (max-width: 1050px) {
  h1.page-heading {
    font-size: 24px !important;
  }
}

.toc {
  background-color: var(--toc-color);
  display: inline-block;
  min-width: 150px;
  width: 100%;
  padding:10px 15px;
  padding-bottom: 0px;
  border-radius: 5px;
  margin-bottom: 13px;
  margin-top: 7px;
  transition: background-color var(--trans-time);

}

.toc-ul {
  list-style-type: none;
  padding-left: 0px;
}

.toc-link {
  color: #3399cc;
  }

@media screen and (max-width: 1280px) {
  .l1 {
    font-size: 24px !important;
  }
}

.l1 {
  font-size: 20px;
  font-weight: bold;
}

.l1 .inline-hashtag {
  height: 18px;
}

@media screen and (max-width: 1280px) {
  .l2 {
    font-size: 20px !important;
  }
}

.l2 {
  padding-left: 13px;
  font-size: 16px;
  text-decoration-style: solid;
}

.l2 .inline-hashtag {
  height: 14px;
}

#toc-title {
  margin-bottom: 0px;
  font-size: 22px;
  font-weight: bold;
}

.hr-1px {
  border-top: 1px solid lightgrey ;
  width: 100%;
  margin-top: 0px;
}

.hr-lowmb {
  margin-bottom: 7px;
  margin-top: 0px;
}
</style>
