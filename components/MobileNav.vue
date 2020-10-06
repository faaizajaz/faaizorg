<template>
  <div id="mobile-nav-div">
    <b-navbar id="mobile-nav" class="d-lg-none fixed-top" toggleable="lg">
      <b-navbar-toggle id="btn-mobile-nav-collapse" target="nav-text-collapse" />
      <span class="mobile-nav-title">Faaiz Ajaz</span>
      <b-navbar-brand>
        <!-- <span class="mobile-nav-title">Faaiz Ajaz</span> -->
        <img class="portrait-mobile" src="~assets/portrait/me.png">
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
          <NuxtLink class="nav-item-mobile nav-link" to="/cv" data-toggle="collapse" data-target=".navbar-collapse.show" exact>
            CV
          </NuxtLink>
          <hr>
          <div id="toggle-wrapper">
            <DarkModeToggle />
          </div>
        </b-navbar-nav>
      </b-collapse>
    </b-navbar>
  </div>
</template>

<script>
import DarkModeToggle from '../components/DarkModeToggle'

export default {
  components: {
    DarkModeToggle
  }
}
</script>

<style>
#mobile-nav {
  background-color: var(--mobile-nav-color);
  padding-top: 0px;
  padding-bottom: 0px;
  padding-right: 15px;
  padding-left: 15px;
  border-bottom: 1px solid #cccccc;
  box-shadow: 0px 3px 5px 0px rgba(0,0,0,0.08);
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
  color: var(--font-color) !important;
  font-size: 20px;
  font-family: 'Bitter', serif;
  padding-bottom: 5px;
  padding-top: 5px;
}

.nav-item-mobile.nuxt-link-active {
  color: var(--accent-color) !important;
  border-left: 10px solid var(--accent-color);
  padding-left: 5px !important;
}

.navbar-toggler-icon {
  background-image: url("~assets/svg/hamburger.svg") !important;
  min-height: 35px;
}

.mobile-nav-title {
  font-family: 'Bitter', serif;
}

#nav-text-collapse {
  padding-bottom: 10px;
}

.navbar-brand {
  margin-right: 0px !important;
}

#toggle-wrapper {
  display: flex;
  justify-content: flex-end;
}

</style>
