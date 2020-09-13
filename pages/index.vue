<template>
  <div class="home-content">
    <MyTestComponent />
    <Aisha />
  </div>
</template>

<script>
import MyTestComponent from '../components/MyTestComponent'
import Aisha from '../components/Aisha'

export default {
  components: {
    MyTestComponent,
    Aisha
  }
}
</script>

<style>
.home-content {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: left;
  align-items: top;
  text-align: left;
}

.title {
  font-family:
    'Quicksand',
    'Source Sans Pro',
    -apple-system,
    BlinkMacSystemFont,
    'Segoe UI',
    Roboto,
    'Helvetica Neue',
    Arial,
    sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
