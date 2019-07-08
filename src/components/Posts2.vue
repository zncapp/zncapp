<template>
  <div class="item">
    <img :src="msg.src"/>
    <strong>{{msg.title}}</strong>
    <p><b>{{msg.name}}</b>{{msg.cont}}</p>
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
  width: 100%
  min-height: 100px
  padding: 15px 10px 15px 100px
  background: rgba(255,255,255,.5)
  border-radius: 5px
  margin-bottom: 12px
  position: relative
  overflow: hidden
  img
    display: block
    @include _wh(80px)
    @include _border(1px,solid,#d5d5d5,50%)
    @include _position(10px,10px)
  strong
    @include _fs(18px,#333)
    font-weight: 700
    line-height: 2
  p
    @include _fs(10px,#555)
    @include _overClamp(3)
    b
      display: inline-block
      margin-right: 10px
      @include _fs(14px,#000)
  label
    display: block
    padding: 5px 10px
    background: #ff6969
    @include _fs(10px,#fff)
    @include _position(0,auto)
    right: 0
    border-radius: 0 0 0 7px
</style>