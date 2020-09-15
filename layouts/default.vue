<template>
  <b-container fluid>
    <b-row>
      <div class="gutter col-xl-2 col-lg-1 d-none d-sm-none d-md-none d-lg-block" />
      <div class="d-none d-sm-none d-md-none d-lg-block col-2 px-1 bg-dark position-fixed offset-xl-2 offset-lg-1">
        <SideNavbar />
      </div>
      <div class="col-xl-6 col-lg-8 offset-xl-2 offset-lg-2">
        <Nuxt />
      </div>
      <div class="gutter col-xl-2 col-lg-1 d-none d-sm-none d-md-none d-lg-block" />
    </b-row>
  </b-container>
</template>

<script>
import SideNavbar from '../components/SideNavbar'

export default {
  components: {
    SideNavbar
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
}

*,
*::before,
*::after {
  box-sizing: border-box;
  margin: 0;
}

.gutter {
    background-color: green;
    min-height: 100vh;
    max-height: 100%;
}
</style>
