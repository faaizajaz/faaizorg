<template>
  <b-container fluid>
    <MobileNav />
    <b-row>
      <div class="gutter col-xl-2 col-lg-1 d-none d-sm-none d-md-none d-lg-block" />
      <div class="sidenav-wrapper d-none d-sm-none d-md-none d-lg-block col-1 position-fixed offset-xl-2 offset-lg-1">
        <SideNavbar />
      </div>
      <div class="content col-xl-7 col-lg-9 offset-xl-1 offset-lg-1">
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
  },
  head: {
    link: [
      {
        rel: 'stylesheet',
        href: 'https://fonts.googleapis.com/css2?family=Bitter:wght@700&family=Source+Sans+Pro&display=swap'
      }
    ],
    title: 'Faaiz Ajaz'
  }
}
</script>

<style>

html {
  font-family: 'Bitter', serif;
  font-family: 'Source Sans Pro', sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
  overflow-y: scroll;
}

@media screen and (max-width: 992px) {
  body {
    padding-top:48px;
  }
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

/*TODO: add some media rules for font size*/
.content {
  font-family: 'Source Sans Pro', sans-serif;
}

@media screen and (max-width: 992px) {
  .content {
    padding-top:8px;
  }
}
@media screen and (min-width: 992px) {
  .content {
    padding-top:26px;
  }
}

.sidenav-wrapper {
  padding-right: 0px;
  min-height: 100vh;
  padding-top: 33px;
}

</style>
