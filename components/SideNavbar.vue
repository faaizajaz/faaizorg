<template>
  <div class="nav flex-column flex-nowrap overflow-auto text-white p-2">
    <NuxtLink to="/blog">
      Blog
    </NuxtLink>
    <NuxtLink to="/about">
      About
    </NuxtLink>
  </div>
</template>

<script>
export default {
  name: 'SideNavbar'
}
</script>

<style>
.nav {
  max-height: 100%;
  min-height: 100vh;
  background-color:lightseagreen;
  border-width: 0px;
}

</style>
