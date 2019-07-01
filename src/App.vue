<template>
  <div id="app">
    <Nav></Nav>
    <div id="center"><router-view/></div>
    <Footer></Footer>
  </div>
</template>

<style lang="sass">
@import "./../public/sass/_sass/_mixin.sass"

html,body,#app
  @include _wh(100%)
.icon
  @include _wh(1em)
  vertical-align: -0.15em
  fill: currentColor
  overflow: hidden
#app
  @include _flex(flex-start)
  flex-direction: column
#center
  width: 100vw
  height: calc(100vh - 30px - 55px)
  overflow: hidden
</style>

<script lang="ts">
import Vue from 'vue';
import Nav from './Nav.vue';
import Footer from './Footer.vue';

export default Vue.extend({
  name: 'app',
  components: {
    Nav,
    Footer,
  },
});
</script>