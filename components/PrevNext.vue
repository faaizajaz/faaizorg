<template>
  <div class="flex justify-content-between">
    <NuxtLink
      v-if="prev"
      :to="{ name: 'blog-slug', params: { slug: prev.slug } }"
      class="previous-link"
    >
      &lt; {{ prev.title }}
    </NuxtLink>
    <span v-else class="empty-blog-link">No previous</span>
    <NuxtLink
      v-if="next"
      :to="{ name: 'blog-slug', params: { slug: next.slug } }"
      class="next-link"
    >
      {{ next.title }} &gt;
    </NuxtLink>
    <span v-else class="empty-blog-link">No next</span>
  </div>
</template>

<script>
export default {
  props: {
    prev: {
      type: Object,
      default: () => null
    },
    next: {
      type: Object,
      default: () => null
    }
  }
}
</script>

<style>

.flex {
  display: flex;
}

.previous-link,
.next-link {
  color: #3399cc;
}

.previous-link,
.next-link,
.empty-blog-link {
  font-weight: bold;
}

</style>
