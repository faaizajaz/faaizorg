<template>
  <div>
    <h5>Author</h5>
    <span>{{ author.name }}</span>
    <p>{{ author.bio }}</p>
  </div>
</template>

<script>
export default {
  props: {
    author: {
      type: Object,
      required: true
    }
  }
}
</script>
