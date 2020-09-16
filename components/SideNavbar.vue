<template>
  <div class="sidebar-div">
    <img src="~assets/portrait/me.png" alt="">
    <ul class="nav flex-column flex-nowrap overflow-auto text-white">
      <li class="nav-item">
        <NuxtLink to="#" class="nav-link">
          Home
        </NuxtLink>
      </li>
      <li class="nav-item">
        <NuxtLink to="#" class="nav-link">
          Projects
        </NuxtLink>
      </li>
      <li class="nav-item">
        <NuxtLink to="/blog" class="nav-link">
          Blog
        </NuxtLink>
      </li>
      <li class="nav-item">
        <NuxtLink to="/about" class="nav-link">
          About
        </NuxtLink>
      </li>
    </ul>
    <div class="social-icons">
      <img class="social-icon" src="~assets/svg/linkedin-grey.svg" alt="">
      <span>&nbsp;</span>
      <img class="social-icon" src="~assets/svg/icon-at-symbol.svg" alt="">
    </div>
  </div>
</template>

<script>
export default {
  name: 'SideNavbar'
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Bitter:wght@700&display=swap');

.nav {
/*   max-height: 100%;
  min-height: 100vh; */
  background-color:white;
  border-width: 0px;
  padding-top: 45px;
}

.nav-item a {
  color: black;
  font-size: 2.8vw;
  font-family: 'Bitter', serif;
}

img {
  border-radius: 50%;
  width: 12vw;
}

.social-icons {
  position: absolute;
  display: flex;
  width: 100%;
  bottom: 20px;
  right: 10px;
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
  padding-left: 15px;

}

</style>
