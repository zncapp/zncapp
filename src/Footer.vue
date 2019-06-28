<template>
  <footer id="footer">
    <router-link v-for="(item, index) in navArr" :key="index" :to="item.to" :class="navIndex === index ? `active` : '' ">
      <svg class="icon" aria-hidden="true">
        <use :xlink:href="`#icon-${item.icon}`"></use>
      </svg>
      {{item.txt}}
    </router-link>
  </footer>
</template>

<script lang="ts">
import Vue from 'vue';

export default Vue.extend({
  name: 'Footer',
  data () {
    return {
      navIndex: 0,
      navArr: [
        { to: '/', icon: 'shenfen', txt: '首页'},
        { to: '/exposure', icon: 'wangshangjubao', txt: '曝光台'},
        { to: '/cooperation', icon: 'qianyueshangpu', txt: '互助圈'}
      ]
    }
  },
  methods: {
  }
});
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="sass">
@import "./../public/sass/_sass/_mixin.sass"
footer
  @include _wh(100vw,55px)
  @include _flex()
  text-align: center
  background: linear-gradient(155deg, #a8edea 0%, #fed6e3 100%)
  a
    flex: 1
    height: 55px
    line-height: 2
    padding: 10px 0 0 0
    @include _flex()
    flex-direction: column
    color: #5b5b5b
    svg
      font-size: 3vh
  a.active
    color: #fff
    background: linear-gradient(0deg, #9795f0 0%, #fbc8d4 80%)
</style>