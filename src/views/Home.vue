<template>
  <div id="home">
    <div class="parent-dom">
      <vueScroll :ops="ops">
        <div class="child-dom">
          <div v-for="(item, index) in msg" :key="index">
            <ShortDisclose :disclose="item"/>
          </div>
        </div>
      </vueScroll>
    </div>
  </div>
</template>

<style lang="sass">
#home
  height: 100%
  background: linear-gradient(155deg, #a8edea 0%, #fed6e3 100%)
  padding: 10px 15px 0
  position: relative
  .parent-dom
    width: 100%
    height: 100%
</style>

<script lang="ts">
import Vue from 'vue';
import vueScroll from 'vuescroll'
import ShortDisclose from '@/components/ShortDisclose.vue'

export default Vue.extend({
  name: 'home',
  components: {
    vueScroll,
    ShortDisclose
  },
  data(){
    return{
      upNum: 0,
      msg: [
        {
          userId: 1,
          label: [
            {type: 10, hot: 6},
            {type: 9, hot: 2}
          ],
          name: '陈某熙',
          sex: 1,
          age: 24,
          place: '北京三里屯',
          education: '北京外国语学院',
          describe: '身高178cm左右，右手腕有痣，喜欢打王者荣耀，养有一只加菲。'
        },
        {
          userId: 2,
          label: [
            {type: 14, hot: 7},
            {type: 18, hot: 10}
          ],
          name: '江某乐',
          sex: 0,
          age: 18,
          place: '北京三里屯',
          education: '北京外国语学院',
          describe: '玩弄感情，双性恋者。诈骗钱财，已有多人上当受害。'
        },
        {
          userId: 3,
          label: [
            {type: 10, hot: 6},
            {type: 9, hot: 2}
          ],
          name: '陈某熙',
          sex: 1,
          age: 24,
          place: '北京三里屯',
          education: '北京外国语学院',
          describe: '身高178cm左右，右手腕有痣，喜欢打王者荣耀，养有一只加菲。'
        },
        {
          userId: 4,
          label: [
            {type: 10, hot: 6},
            {type: 9, hot: 2}
          ],
          name: '陈某熙',
          sex: 1,
          age: 24,
          place: '北京三里屯',
          education: '北京外国语学院',
          describe: '身高178cm左右，右手腕有痣，喜欢打王者荣耀，养有一只加菲。'
        },
      ],
      ops:{
        vuescroll: {
          mode: 'slide',
          sizeStrategy: 'percent',
          detectResize: true,
        },
        scrollPanel: {
          initialScrollY: false,
          initialScrollX: false,
          scrollingX: false,
          scrollingY: true,
          speed: 1000,
          easing: 'easeInQuad',
          verticalNativeBarPos: 'right'
        },
        rail: {
          background: '#fff',
          opacity: 0,
          size: '1px',
          specifyBorderRadius: false,
          gutterOfEnds: null,
          gutterOfSide: '0px',
          keepShow: false
        },
        bar: {
          showDelay: 200,
          onlyShowBarOnScroll: true,
          keepShow: false,
          background: '#000',
          opacity: 0.5,
          hoverStyle: false,
          specifyBorderRadius: false,
          minSize: false,
          size: '3px',
          disable: false,
        }
      }
    }
  }
});
</script>
