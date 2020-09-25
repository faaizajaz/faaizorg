<template>
  <div id="copyright-div">
    <span class="copyright-info">Copyright© 2020<br>Faaiz Ajaz</span>
  </div>
</template>

<script>
export default {

}
</script>

<style>
#copyright-div {
  position: absolute;
  display: flex;
  justify-content: center;
  width: 100%;
  bottom: 15px;
  right: 14px;
  font-family: 'Source Sans Pro', sans-serif;
  color: grey;

}

@media screen and (min-width: 1200px) {
  #copyright-div {
    font-size: 10.5px;
  }
}

@media screen and (min-width: 993px) and (max-width: 1200px) {
  #copyright-div {
    font-size: 0.65vw;
  }
}

</style>
