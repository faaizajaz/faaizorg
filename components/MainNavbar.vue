<template>
  <b-container fluid="lg">
    <b-navbar toggleable="lg" type="dark">
      <b-navbar-brand href="#">
        Faaiz Ajaz
      </b-navbar-brand>

      <b-navbar-toggle target="nav-collapse" />

      <b-collapse id="nav-collapse" is-nav>
        <!-- Right aligned nav items -->
        <b-navbar-nav class="ml-auto">
          <b-nav-item href="#">
            Link
          </b-nav-item>
          <b-nav-item href="#">
            Link
          </b-nav-item>
        </b-navbar-nav>
      </b-collapse>
    </b-navbar>
  </b-container>
</template>

<script>
export default {

  name: 'MainNavbar',

  data () {
    return {
    }
  }
}
</script>

<style lang="css" scoped>
  .navbar {
    background-color: hotpink;
  }
</style>
