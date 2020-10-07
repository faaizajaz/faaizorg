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
      <DarkModeToggle />
    </div>
  </span>
</template>

<script>
import DarkModeToggle from '../components/DarkModeToggle'

export default {
  name: 'SideNavbar',
  components: {
    DarkModeToggle
  }
}
</script>

<style>

.nav {
/*   max-height: 100%;
  min-height: 100vh; */
  background-color: var(--content-color);
  border-width: 0px;
  padding-top: 0px;
}

.nav-item-regular a {
  color: var(--font-color);
  font-family: 'Bitter', serif;
}

@media screen and (min-width: 1200px) {
  .nav-item-regular a {
    font-size: 1.70vw;
  }
}

@media screen and (min-width: 1051px) and (max-width: 1200px) {
  .nav-item-regular a {
    font-size: 1.60vw;
    padding-top: 5px;
    padding-bottom: 5px;
  }
}

.portrait {
  border-radius: 50%;
  width: 100%;
  margin-bottom: 15px;
}

.portrait-div {
  /* position: absolute; */
  display: flex;
  width: 100%;
  /* right: 10px; */
  justify-content: center;
}

/* #sidebar-div {
  min-height: 100vh;
  position: relative;
  padding-top: 40px;
  padding-bottom: 20px;
  padding-left: 25px;

} */

/* @media screen and (min-width: 1300px) {
  a.nav-link {
    padding-left:40px;
  }
} */

a.nav-link {
  padding-left: 0px;
}

.nav-item-regular .nuxt-link-active {
  color: var(--accent-color) !important;
  /* border-left: 10px solid #3399cc; */
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
  color: var(--accent-color);
}

#sidebar-footer {
  position: absolute;
  display: flex;
  justify-content: center;
  bottom: 15px;
  height: auto;
  width: 100%;
  margin-left: -10px;
}

.sidenav-wrapper {
  box-shadow: -12px 0 10px -4px rgba(0,0,0,var(--shadow));
  padding-left: 20px;
}

</style>
