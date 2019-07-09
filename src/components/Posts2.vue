<template>
  <div class="item">
    <img :src="msg.src"/>
    <strong>{{msg.title}}</strong>
    <font>{{msg.time}}</font>
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
  width: 100%
  min-height: 50px
  padding: 5px 65px 10px 50px
  background: rgba(255,255,255,.5)
  border-radius: 5px
  margin-bottom: 12px
  position: relative
  overflow: hidden
  img
    display: block
    @include _wh(30px)
    @include _border(1px,solid,#d5d5d5,5px)
    @include IamTheTable
    left: 10px
  strong
    @include _fs(12px,#333)
    font-weight: 700
    line-height: 1
  p
    @include _fs(8px,#555)
    @include _overClamp(3)
    padding: 5px 0 0 0
  font
    @include _fs(10px,#999)
    @include IamTheTable
    right: 10px
  label
    display: block
    padding: 2px 10px
    background: #ff6969
    @include _fs(10px,#fff)
    @include _position(0,auto)
    right: 0
    border-radius: 0 0 0 7px
</style>