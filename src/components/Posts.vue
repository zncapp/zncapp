<template>
  <div class="item">
    <img :src="msg.src"/>
    <strong>{{msg.title}}</strong>
    <p>{{msg.cont}}</p>
    <label v-if="msg.top">置顶</label>
  </div>
</template>

<script lang="ts">
import Vue from 'vue';

export default Vue.extend({
  name: 'PostsItem',
  props: {
    msg: Object 
  }
});
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="sass">
@import "./../../public/sass/_sass/_mixin.sass"
.item
  @include _wh(100%,auto)
  padding: 5px
  background: rgba(255,255,255,.5)
  border-radius: 5px
  margin-bottom: 12px
  position: relative
  overflow: hidden
  img
    display: block
    @include _wh(100%,auto)
    @include _border(1px,solid,#d5d5d5,3px)
  strong
    @include _fs(18px,#333)
    font-weight: 700
    line-height: 2
  p
    padding: 0 7px
    @include _fs(10px,#555)
    @include _overClamp(2)
  label
    display: block
    padding: 5px 10px
    background: #ff6969
    @include _fs(10px,#fff)
    @include _position(0,auto)
    right: 0
    border-radius: 0 0 0 7px
</style>