<template>
  <div>
    <div id="author">
      <span>by {{ author.name }} on {{ created }}</span>
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
    created: {
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
  font-size: 14px;
}

</style>
