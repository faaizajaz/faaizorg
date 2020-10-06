<template>
  <div class="dark-toggle-div">
    <img class="dark-toggle-icons icon" src="~assets/svg/light/sun-light.svg">
    <label class="switch" @change="switchTheme">
      <input type="checkbox">
      <span class="slider round" />
    </label>
    <img class="dark-toggle-icons" src="~assets/svg/light/moon-light.svg">
  </div>
</template>

<script>
export default {
  name: 'DarkModeToggle',
  methods: {
    switchTheme (e) {
      if (e.target.checked) {
        document.documentElement.setAttribute('data-theme', 'dark')
      } else {
        document.documentElement.setAttribute('data-theme', '')
      }
    }
  }
}
</script>

<style lang="css">
/* The switch - the box around the slider */
.switch {
  position: relative;
  display: inline-block;
  width: 30px;
  height: 20px;
}

/* Hide default HTML checkbox */
.switch input {
  opacity: 0;
  width: 0;
  height: 0;
}

/* The slider */
.slider {
  position: absolute;
  cursor: pointer;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background-color: #ccc;
  -webkit-transition: .3s;
  transition: all .3s;
}

.slider::before {
  position: absolute;
  content:  "";
  height: 14px;
  width: 14px;
  left: 3px;
  bottom: 3px;
  background-color: white;
  -webkit-transition: .3s;
}

input:checked + .slider {
  background-color: var(--accent-color);
}

input:checked + .slider::before {
  -webkit-transform: translateX(20px);
  -ms-transform: translateX(20px);
  transform: translateX(10px);
}

/* Rounded sliders */
.slider.round {
  border-radius: 25px;
}

.slider.round::before {
  border-radius: 50%;
}

.dark-toggle-icons {
  height: 15px;
  width: 15px;
  margin-bottom: 7px;

}

</style>
