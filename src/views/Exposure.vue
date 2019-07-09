<template>
  <div id="Exposure">
    <div class="parent-dom">
      <vueScroll :ops="ops">
        <div class="child-dom">
          <div v-for="(item, index) in msg" :key="index">
            <Posts2 :msg="item"></Posts2>
          </div>
        </div>
      </vueScroll>
    </div>
  </div>
</template>

<style lang="sass">
#Exposure
  height: 100%
  background: linear-gradient(155deg, #d299c2 0%, #fef9d7 100%)
  padding: 10px 15px 0
  position: relative
  .parent-dom
    width: 100%
    height: 100%
</style>

<script lang="ts">
import Vue from 'vue';
import vueScroll from 'vuescroll'
import Posts2 from '@/components/Posts2.vue';

export default Vue.extend({
  name: 'Exposure',
  components: {
    vueScroll,
    Posts2
  },
  data(){
    return{
      msg: [
        {
          id: 1,
          top: true,
          time: '2019-06-03',
          src: './img/img2.png',
          title: '泰国孕妇坠崖事件始末:丈夫涉嫌杀人未遂',
          cont: '王女士怎么也想不到，一次对她来说轻车熟路的泰国之行，会让她从乌汶府国家公园高达34米的悬崖坠落，凭侥幸才捡回一条命。'
        },
        {
          id: 2,
          top: false,
          time: '2019-06-03',
          src: './img/img2.png',
          title: '男子泰国杀妻骗保，开庭否认蓄意谋杀自辩激情杀人',
          cont: '天津男子普吉岛杀妻骗保案”7月5日上午9点在泰国普吉府法院正式开庭审理。'
        },
        {
          id: 3,
          top: false,
          time: '2019-06-03',
          src: './img/img2.png',
          title: '男子泰国杀妻骗保，开庭否认蓄意谋杀自辩激情杀人',
          cont: '天津男子普吉岛杀妻骗保案”7月5日上午9点在泰国普吉府法院正式开庭审理。'
        },
        {
          id: 4,
          top: false,
          time: '2019-06-03',
          src: './img/img2.png',
          title: '男子泰国杀妻骗保，开庭否认蓄意谋杀自辩激情杀人',
          cont: '天津男子普吉岛杀妻骗保案”7月5日上午9点在泰国普吉府法院正式开庭审理。'
        },
        {
          id: 5,
          top: false,
          time: '2019-06-03',
          src: './img/img2.png',
          title: '男子泰国杀妻骗保，开庭否认蓄意谋杀自辩激情杀人',
          cont: '天津男子普吉岛杀妻骗保案”7月5日上午9点在泰国普吉府法院正式开庭审理。'
        },
        {
          id: 6,
          top: false,
          time: '2019-06-03',
          src: './img/img2.png',
          title: '男子泰国杀妻骗保，开庭否认蓄意谋杀自辩激情杀人',
          cont: '天津男子普吉岛杀妻骗保案”7月5日上午9点在泰国普吉府法院正式开庭审理。'
        },
        {
          id: 7,
          top: false,
          time: '2019-06-03',
          src: './img/img2.png',
          title: '男子泰国杀妻骗保，开庭否认蓄意谋杀自辩激情杀人',
          cont: '天津男子普吉岛杀妻骗保案”7月5日上午9点在泰国普吉府法院正式开庭审理。'
        },
        {
          id: 8,
          top: false,
          time: '2019-06-03',
          src: './img/img2.png',
          title: '男子泰国杀妻骗保，开庭否认蓄意谋杀自辩激情杀人',
          cont: '天津男子普吉岛杀妻骗保案”7月5日上午9点在泰国普吉府法院正式开庭审理。'
        },
        {
          id: 9,
          top: false,
          time: '2019-06-03',
          src: './img/img2.png',
          title: '男子泰国杀妻骗保，开庭否认蓄意谋杀自辩激情杀人',
          cont: '天津男子普吉岛杀妻骗保案”7月5日上午9点在泰国普吉府法院正式开庭审理。'
        },
        {
          id: 10,
          top: false,
          time: '2019-06-03',
          src: './img/img2.png',
          title: '男子泰国杀妻骗保，开庭否认蓄意谋杀自辩激情杀人',
          cont: '天津男子普吉岛杀妻骗保案”7月5日上午9点在泰国普吉府法院正式开庭审理。'
        }
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