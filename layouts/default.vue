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
import '../assets/scss/breakpoints.scss'

export default {
  components: {
    SideNavbar,
    MobileNav
  },
  head () {
    return {
      link: [
        {
          rel: 'stylesheet',
          href: 'https://fonts.googleapis.com/css2?family=Bitter:wght@700&family=Source+Sans+Pro&display=swap'
        },
        {
          rel: 'canonical',
          href: 'https://faaiz.org' + this.$route.path
        }
      ],
      title: 'Faaiz Ajaz'
    }
  }
}

</script>

<style>
/** VARIABLES **/

:root {
  --content-color: #ffffff;
  --gutter-color: #efefef;
  --mobile-nav-color: #ffffff;
  --toc-color: #efefef;
  --font-color: #202429;
  --accent-color: #3399cc;
  --shadow: 0.08;
}

[data-theme="dark"] {
  --content-color: #2f2f2f;
  --gutter-color: #3e3e3e;
  --mobile-nav-color: #545454;
  --toc-color: #3e3e3e;
  --font-color: #dcdcdc;
  --accent-color: #3399cc;
  --shadow: 0.40;
}

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
  --trans-time:  0.3s;
}

@media screen and (max-width: 1050px) {
  body {
    padding-top:48px;
  }
}

body {
  font-size: 15pt;
  background-color: var(--content-color);
  color: var(--font-color);
  transition: background-color var(--trans-time), color var(--trans-time);
}

*,
*::before,
*::after {
  box-sizing: border-box;
  margin: 0;
}

.gutter {
    background-color: var(--gutter-color);
    min-height: 100vh;
    max-height: 100%;
    transition: background-color var(--trans-time);
}

/*TODO: add some media rules for font size*/
.content {
  font-family: 'Source Sans Pro', sans-serif;
  box-shadow: 12px 0 10px -4px rgba(0,0,0,var(--shadow));
  z-index: 1;
  transition: box-shadow var(--trans-time);
}

@media screen and (max-width: 1050px) {
  .content {
    padding-top:15px;
    padding-left: 10px;
    padding-right: 10px;
    min-height: calc(100vh - 48px);
  }
}
@media screen and (min-width: 1051px) {
  .content {
    padding-top:28px;
    padding-left: 20px;
    padding-right: 15px;
  }
}

.sidenav-wrapper {
  padding-right: 0px;
  min-height: 100vh;
  padding-top: 33px;
}

hr {
  border-color: var(--toc-color);
  transition: border-color var(--trans-time);
}

</style>
