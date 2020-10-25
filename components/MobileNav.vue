<template>
  <div id="mobile-nav-div">
    <b-navbar id="mobile-nav" class="d-lg-none fixed-top" toggleable="lg">
      <b-navbar-toggle id="btn-mobile-nav-collapse" target="nav-text-collapse">
        <svg
          id="hamburger-icon"
          height="32px"
          style="enable-background:new 0 0 32 32;"
          version="1.1"
          viewBox="0 0 32 32"
          width="32px"
          xml:space="preserve"
          xmlns="http://www.w3.org/2000/svg"
          xmlns:xlink="http://www.w3.org/1999/xlink"
        >
          <path d="M4,10h24c1.104,0,2-0.896,2-2s-0.896-2-2-2H4C2.896,6,2,6.896,2,8S2.896,10,4,10z M28,14H4c-1.104,0-2,0.896-2,2  s0.896,2,2,2h24c1.104,0,2-0.896,2-2S29.104,14,28,14z M28,22H4c-1.104,0-2,0.896-2,2s0.896,2,2,2h24c1.104,0,2-0.896,2-2  S29.104,22,28,22z" />
        </svg>
      </b-navbar-toggle>
      <span class="mobile-nav-title">Faaiz Ajaz</span>
      <b-navbar-brand>
        <!-- <span class="mobile-nav-title">Faaiz Ajaz</span> -->
        <img class="portrait-mobile" src="~assets/portrait/Faaiz_Ajaz_Hunza.png" alt="An image of Faaiz Ajaz above the Hunza Valley">
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
  padding-right: 10px;
  padding-left: 10px;
  border-bottom: 1px solid var(--toc-color);
  box-shadow: 0px 3px 5px 0px rgba(0,0,0,var(--shadow));
  transition: background-color var(--trans-time), border-color var(--trans-time);
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
  transition: color var(--trans-time);
}

.nav-item-mobile.nuxt-link-active {
  color: var(--accent-color) !important;
  border-left: 10px solid var(--accent-color);
  padding-left: 5px !important;
}

.navbar-toggler-icon {
  min-height: 35px;
}

#hamburger-icon {
  fill: var(--font-color) !important;
}

.mobile-nav-title {
  font-family: 'Bitter', serif;
}

.navbar-brand {
  margin-right: 0px !important;
}

#toggle-wrapper {
  display: flex;
  justify-content: flex-end;
  padding-bottom: 15px;
}

</style>
