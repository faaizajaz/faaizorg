<template>
  <b-container fluid>
    <MobileNav />
    <b-row>
      <div class="gutter col-xl-2 col-lg-1 d-none d-sm-none d-md-none d-lg-block" />
      <div class="d-none d-sm-none d-md-none d-lg-block col-2 px-1 position-fixed offset-xl-2 offset-lg-1">
        <SideNavbar />
      </div>
      <div class="content col-xl-6 col-lg-8 offset-xl-2 offset-lg-2">
        <Nuxt />
      </div>
      <div class="gutter col-xl-2 col-lg-1 d-none d-sm-none d-md-none d-lg-block" />
    </b-row>
  </b-container>
</template>

<script>
import SideNavbar from '../components/SideNavbar'
import MobileNav from '../components/MobileNav'

export default {
  components: {
    SideNavbar,
    MobileNav
  }
}
</script>

<style>
html {
  font-family:
    'Source Sans Pro',
    -apple-system,
    BlinkMacSystemFont,
    'Segoe UI',
    Roboto,
    'Helvetica Neue',
    Arial,
    sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
  overflow-y: scroll;
}

*,
*::before,
*::after {
  box-sizing: border-box;
  margin: 0;
}

.gutter {
    background-color: white;
    min-height: 100vh;
    max-height: 100%;
}

.content {
  padding-left: 0px;
}
</style>
