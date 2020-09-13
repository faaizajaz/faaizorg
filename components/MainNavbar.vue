<template>
  <!--   <b-container fluid="lg"> -->
  <b-navbar toggleable="lg" type="dark">
    <nuxt-link to="/" class="logo">
      Faaiz Ajaz
    </nuxt-link>

    <b-navbar-toggle target="nav-collapse" />

    <b-collapse id="nav-collapse" is-nav>
      <!-- Right aligned nav items -->
      <b-navbar-nav class="ml-auto">
        <nuxt-link to="/blog">
          Blog
        </nuxt-link>
        <nuxt-link to="/about">
          About
        </nuxt-link>
      </b-navbar-nav>
    </b-collapse>
  </b-navbar>
<!--   </b-container> -->
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

.navbar-nav a {
  color: lightgrey;
  text-decoration: none;
  margin-left: 10px;
  margin-right: 10px;
}

.navbar-nav a:active {
  color: white;
}

.navbar-nav a:hover {
  color: white;
}

.logo {
  color: white;
  font-size: 24px;
  text-decoration: none;
}
</style>
