<template>
  <div id="home-content">
    <h1 class="page-heading">
      About me
    </h1>
    <BarDivider />
    <div>
      <h2>My name is Faaiz</h2>
      Faaiz rhymes with:
      <ul>
        <li>eyes</li>
        <li>thighs</li>
        <li>spies</li>
        <li>lies</li>
      </ul>
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

<style scoped>
#home-content {
  margin: 0 auto;
  /* min-height: 100vh; */
/*   display: flex;
  justify-content: left;
  align-items: top; */
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

</style>
