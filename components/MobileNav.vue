<template>
  <b-navbar id="mobile-nav" class="d-lg-none fixed-top" toggleable="lg">
    <b-navbar-toggle target="nav-text-collapse" />

    <b-navbar-brand>
      <img class="portrait-mobile" src="~assets/portrait/me.png" alt="">
    </b-navbar-brand>

    <b-collapse id="nav-text-collapse" is-nav>
      <b-navbar-nav>
        <b-nav-item class="nav-item-mobile">
          <NuxtLink to="/" data-toggle="collapse" data-target=".navbar-collapse.show" exact>
            Home
          </NuxtLink>
        </b-nav-item>
        <b-nav-item class="nav-item-mobile">
          <NuxtLink to="/projects" data-toggle="collapse" data-target=".navbar-collapse.show" exact>
            Projects
          </NuxtLink>
        </b-nav-item>
        <b-nav-item class="nav-item-mobile">
          <NuxtLink to="/blog" data-toggle="collapse" data-target=".navbar-collapse.show">
            Blog
          </NuxtLink>
        </b-nav-item>
        <b-nav-item class="nav-item-mobile">
          <NuxtLink to="/about" data-toggle="collapse" data-target=".navbar-collapse.show" exact>
            About
          </NuxtLink>
        </b-nav-item>
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
  padding-top: 0px;
  padding-bottom: 0px;
  padding-right: 0px;
  padding-left: 15px
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

.nav-item-mobile a {
  color: black;
  font-size: 2vh;
  font-family: 'Bitter', serif;
  padding-bottom: 5px;
  padding-top: 0px;
}
</style>
