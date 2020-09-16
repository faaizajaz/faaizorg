<template>
  <b-navbar id="mobile-nav" class="d-lg-none" toggleable="lg">
    <b-navbar-toggle target="nav-text-collapse" />

    <b-navbar-brand>Faaiz.org</b-navbar-brand>

    <b-collapse id="nav-text-collapse" is-nav>
      <b-navbar-nav>
        <b-nav-text>
          <NuxtLink to="/blog">
            Blog
          </NuxtLink>
        </b-nav-text>
        <b-nav-text>
          <NuxtLink to="/about">
            About
          </NuxtLink>
        </b-nav-text>
      </b-navbar-nav>
    </b-collapse>
  </b-navbar>
</template>

<script>
export default {

}
</script>

<style>
#mobile-nav {
  background-color: lightseagreen;
}

</style>
