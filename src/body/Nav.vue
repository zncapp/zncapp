<template>
  <nav id="nav">
    <div>搜索框</div>
    <div>我的</div>
  </nav>
</template>

<script lang="ts">
import Vue from 'vue';

export default Vue.extend({
  name: 'Nav'
});
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="sass">
@import "./../../public/sass/_sass/_mixin.sass"
nav
  @include _wh(100vw,30px)
  @include _flex()
  padding: 0 15px
  background: linear-gradient(90deg, rgba(10, 207, 254, .5) 0%, rgba(73, 90, 255, .5) 100%)
  box-shadow: 0 0.04rem 0.266667rem 0 rgba(0, 0, 0, .1)
</style>