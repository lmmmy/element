<template>
  <div id="app">
     <v-header></v-header>
    <v-commodity></v-commodity>
    <v-footer></v-footer>
  </div>
</template>

<script>
import header from './components/header/header.vue';
import commodity from './components/commodity/commodity.vue';
import footer from './components/footer/footer.vue';
export default {
  components: {
    'v-header': header,
    'v-commodity': commodity,
    'v-footer': footer
  },
  name: 'app'
};
window.addEventListener('orientationchange', setRem);
window.addEventListener('resize', setRem);
setRem();
function setRem () {
  var html = document.querySelector('html');
  var width = html.getBoundingClientRect().width;
  html.style.fontSize = width / 15 + 'px';
};
</script>

<style>
  @import "common/css/main.css";
  @import "common/css/reset.css";
</style>
