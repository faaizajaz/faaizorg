<template>
  <span>
    <div class="portrait-div">
      <img class="portrait" src="~assets/portrait/me.png" alt="">
    </div>
    <ul class="nav flex-column flex-nowrap overflow-auto text-white">
      <li class="nav-item-regular">
        <NuxtLink to="/" class="nav-link" exact>
          About
        </NuxtLink>
      </li>
      <li class="nav-item-regular">
        <NuxtLink to="/projects" class="nav-link" exact>
          Projects
        </NuxtLink>
      </li>
      <li class="nav-item-regular">
        <NuxtLink to="/blog" class="nav-link">
          Blog
        </NuxtLink>
      </li>
      <li class="nav-item-regular">
        <NuxtLink to="/cv" class="nav-link" exact>
          CV
        </NuxtLink>
      </li>
    </ul>
    <div id="sidebar-footer">
      <SocialIcons />
      <CopyrightInfo />
    </div>
  </span>
</template>

<script>
import CopyrightInfo from '../components/CopyrightInfo'
import SocialIcons from '../components/SocialIcons'

export default {
  name: 'SideNavbar',
  components: {
    CopyrightInfo,
    SocialIcons
  }
}
</script>

<style>

.nav {
/*   max-height: 100%;
  min-height: 100vh; */
  background-color:white;
  border-width: 0px;
  padding-top: 275px;
}

.nav-item-regular a {
  color: black;
  font-size: calc(5px + 1.9vw);
  font-family: 'Bitter', serif;
}

.portrait {
  border-radius: 50%;
  width: 11.5vw;
}

.portrait-div {
  position: absolute;
  display: flex;
  width: 100%;
  right: 10px;
  justify-content: center;
}

/* #sidebar-div {
  min-height: 100vh;
  position: relative;
  padding-top: 40px;
  padding-bottom: 20px;
  padding-left: 25px;

} */

@media screen and (min-width: 1300px) {
  a.nav-link {
    padding-left:40px;
  }
}

.nav-item-regular .nuxt-link-active {
  color: #3399cc !important;
  border-left: 10px solid #3399cc;
/*   padding-top: 0px;
  padding-bottom: 0px; */
}

/* @keyframes example {
  from {padding-left: 40px;}
  to {padding-left: 50px;}
}
:not(.nuxt-link-active).nav-link:hover {
  animation-name: example;
  animation-duration: 50ms;
  animation-fill-mode: forwards
} */
.nav-link:hover {
  color: #3399cc;
}
</style>
