<template>
  <div class="items">
    <strong>{{msg.title}}</strong>
    <p>{{msg.cont}}</p>
    <font>{{msg.time}}</font>
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
.items
  @include _wh(100%,auto)
  padding: 5px 65px 9px 9px
  background: rgba(255,255,255,.5)
  border-radius: 5px
  margin-bottom: 12px
  position: relative
  overflow: hidden
  strong
    @include _fs(12px,#333)
    font-weight: 700
    line-height: 1
  p
    @include _fs(10px,#555)
    @include _overClamp(2)
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