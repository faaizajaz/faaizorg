<template>
  <div class="sidebar-div">
    <div class="portrait-div">
      <img class="portrait" src="~assets/portrait/me.png" alt="">
    </div>
    <ul class="nav flex-column flex-nowrap overflow-auto text-white">
      <li class="nav-item">
        <NuxtLink to="/" class="nav-link" exact>
          Home
        </NuxtLink>
      </li>
      <li class="nav-item">
        <NuxtLink to="/projects" class="nav-link" exact>
          Projects
        </NuxtLink>
      </li>
      <li class="nav-item">
        <NuxtLink to="/blog" class="nav-link">
          Blog
        </NuxtLink>
      </li>
      <li class="nav-item">
        <NuxtLink to="/about" class="nav-link" exact>
          About
        </NuxtLink>
      </li>
    </ul>
    <div class="social-icons">
      <a href="https://www.linkedin.com/in/faaizajaz/">
        <img class="social-icon" src="~assets/svg/linkedin-grey.svg" alt="LinkedIn">
      </a>
      <span>&nbsp;</span>
      <a href="mailto:faaizajaz@gmail.com">
        <img class="social-icon" src="~assets/svg/icon-at-symbol.svg" alt="Email">
      </a>
    </div>
  </div>
</template>

<script>
export default {
  name: 'SideNavbar'
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

.nav-item a {
  color: black;
  font-size: calc(5px + 2.1vw);
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

.social-icons {
  position: absolute;
  display: flex;
  width: 100%;
  bottom: 20px;
  right: 14px;
  justify-content: center;
}

.social-icon {
  width: 20px;
}

.sidebar-div {
  min-height: 100vh;
  position: relative;
  padding-top: 40px;
  padding-bottom: 20px;
  padding-left: 25px;

}

.nuxt-link-active {
  background-color:darkolivegreen;
}

</style>
