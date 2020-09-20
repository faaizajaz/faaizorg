<template>
  <div>
    <div id="author">
      <span>Posted by: {{ author.name }} on {{ updated }}</span>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    author: {
      type: Object,
      required: true
    },
    updated: {
      type: String,
      default: () => null
    }
  }
}
</script>

<style scoped>
#author {
  width: 100%;
  text-align: right;
  color: grey;
  font-style: italic;
}

</style>
