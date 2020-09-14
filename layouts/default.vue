<template>
  <b-container>
    <b-row>
      <MainNavbar />
      <b-col class="no-margin" cols="12" md="3">
        <SideNavbar />
      </b-col>
      <b-col class="no margin" cols="12" md="9">
        <Nuxt />
      </b-col>
    </b-row>
  </b-container>
</template>

<script>
import MainNavbar from '../components/MainNavbar'
import SideNavbar from '../components/SideNavbar'

export default {
  components: {
    MainNavbar,
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

.container {
/*   max-width: 1300px; */
  padding:  0px;
}
</style>
