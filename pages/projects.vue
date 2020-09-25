<template>
  <div>
    <h1 class="page-heading">
      Projects
    </h1>
    <BarDivider />
    <div>
      <h2>Believe me</h2>
      <p>
        There are a few.
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
