<template>
  <div id="home-content">
    <h1 class="page-heading">
      About me
    </h1>
    <BarDivider />
    <div>
      <h1>Faaiz Ajaz <small>[faɪz ɪˈd͡ʒaz]</small></h1>
      <p>
        My name is Faaiz, which rhymes with fries or lies or spies. I am an international development consultant working in the climate change and disaster risk reduction space. You can find out more by checking out my CV
        <NuxtLink to="/cv">
          here,
        </NuxtLink>
        or&mdash;because it's 2020 and everything is social media&mdash;you can visit my LinkedIn profile <a href="https://www.linkedin.com/in/faaizajaz/">here.</a>
      </p>
      <p>
        I made this website to take back some control of my internet search results. If this page isn't the first result returned when you search for 'Faaiz Ajaz' on your choice of search engine, then I have not yet succeeded in doing so.
      </p>
      <p>
        It is more difficult than it sounds.
      </p>
    </div>
  </div>
</template>

<script>
import BarDivider from '../components/BarDivider'

export default {
  components: {
    BarDivider
  }
}
</script>

<style scoped>
#home-content {
  margin: 0 auto;
  /* min-height: 100vh; */
/*   display: flex;
  justify-content: left;
  align-items: top; */
  text-align: left;
}

.page-heading {
  font-family: 'Bitter', serif;
  text-align: left;
}

@media screen and (max-width: 1050px) {
  h1.page-heading {
    font-size: 24px !important;
  }
}

a {
    color: #3399cc;
    font-weight: bold;
}

</style>
