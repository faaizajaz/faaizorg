<template>
  <b-navbar id="mobile-nav" class="d-lg-none fixed-top" toggleable="lg">
    <b-navbar-toggle target="nav-text-collapse" />

    <b-navbar-brand>
      <img class="portrait-mobile" src="~assets/portrait/me.png" alt="">
    </b-navbar-brand>

    <b-collapse id="nav-text-collapse" is-nav>
      <b-navbar-nav>
        <b-nav-text>
          <NuxtLink to="/" exact>
            Home
          </NuxtLink>
        </b-nav-text>
        <b-nav-text>
          <NuxtLink to="/projects" exact>
            Projects
          </NuxtLink>
        </b-nav-text>
        <b-nav-text>
          <NuxtLink to="/blog">
            Blog
          </NuxtLink>
        </b-nav-text>
        <b-nav-text>
          <NuxtLink to="/about" exact>
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
  background-color: white;
  padding: 0px 0px;
}

.nuxt-link-active {
  background-color:darkolivegreen;
}

.portrait-mobile {
  border-radius: 50%;
  width: 10vw;
  max-height: 58px;
  max-width: 58px
}
</style>
