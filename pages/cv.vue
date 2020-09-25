<template>
  <div>
    <h1 class="page-heading">
      Curriculum Vitae
    </h1>
    <BarDivider />
    <div>
      <h2>I promise</h2>
      <p>
        My CV will be here eventually.
      </p>
    </div>
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

@media screen and (max-width: 991px) {
  h1.page-heading {
    font-size: 24px !important;
  }
}

</style>
