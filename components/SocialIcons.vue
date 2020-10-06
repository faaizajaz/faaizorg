<template>
  <div class="social-icons">
    <a href="https://www.github.com/faaizajaz/">
      <img class="social-icon" src="~assets/svg/github-logo.svg" alt="GitHub">
    </a>
    <span>&nbsp;</span>
    <span>&nbsp;</span>
    <a href="https://www.linkedin.com/in/faaizajaz/">
      <img class="social-icon" src="~assets/svg/linkedin-black.svg" alt="LinkedIn">
    </a>
    <span>&nbsp;</span>
    <span>&nbsp;</span>
    <a href="mailto:faaizajaz@gmail.com">
      <img class="social-icon" src="~assets/svg/at-symbol.svg" alt="Email">
    </a>
  </div>
</template>

<script>
export default {
  name: 'SocialIcons'
}
</script>

<style>
.social-icons {
  position: absolute;
  display: flex;
  width: 100%;
  bottom: 20px;
  right: auto;
  left:  auto;
  justify-content: center;
}

.social-icon {
  width: calc(5px + 1vw);
}
</style>
