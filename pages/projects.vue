<template>
  <div>
    <h1 class="page-heading">
      Projects
    </h1>
    <BarDivider />
  </div>
</template>

<script>
import BarDivider from '../components/BarDivider'

export default {
  components: {
    BarDivider
  }

}
</script>

<style>
.page-heading {
  font-family: 'Bitter', serif;
  text-align: left;
}

@media screen and (max-width: 1050px) {
  h1.page-heading {
    font-size: 24px !important;
  }
}

</style>
