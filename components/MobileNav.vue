<template>
  <div id="mobile-nav-div">
    <b-navbar id="mobile-nav" class="d-lg-none fixed-top" toggleable="lg">
      <b-navbar-toggle id="btn-mobile-nav-collapse" target="nav-text-collapse" />

      <b-navbar-brand>
        <img class="portrait-mobile" src="~assets/portrait/me.png" alt="">
      </b-navbar-brand>

      <b-collapse id="nav-text-collapse" is-nav>
        <b-navbar-nav>
          <NuxtLink class="nav-item-mobile nav-link" to="/" data-toggle="collapse" data-target=".navbar-collapse.show" exact>
            About
          </NuxtLink>
          <NuxtLink class="nav-item-mobile nav-link" to="/projects" data-toggle="collapse" data-target=".navbar-collapse.show" exact>
            Projects
          </NuxtLink>
          <NuxtLink class="nav-item-mobile nav-link" to="/blog" data-toggle="collapse" data-target=".navbar-collapse.show">
            Blog
          </NuxtLink>
          <NuxtLink class="nav-item-mobile nav-link" to="/resume" data-toggle="collapse" data-target=".navbar-collapse.show" exact>
            Résumé
          </NuxtLink>
        </b-navbar-nav>
      </b-collapse>
    </b-navbar>
  </div>
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
  padding-left: 15px;
  border-bottom: 1px solid #cccccc;
}

.portrait-mobile {
  border-radius: 50%;
  width: 37px;
  height: 37px;
}

#btn-mobile-nav-collapse {
  max-height: 58px;
  max-width: 58px;
  border: 0px;
  padding-left: 0px;
}

#btn-mobile-nav-collapse {
  outline: 0px;
}

.nav-item-mobile.nav-link {
  color: black !important;
  font-size: 2vh;
  font-family: 'Bitter', serif;
  padding-bottom: 5px;
  padding-top: 0px;
}

.nav-item-mobile.nuxt-link-active {
  color: #3399cc !important;
}

.navbar-toggler-icon {
  background-image: url("~assets/svg/hamburger.svg") !important;
  min-height: 35px;
}

</style>
