<template>
  <div id="Cooperation">
    <div class="parent-dom">
      <vueScroll :ops="ops">
        <div class="child-dom">
          <div v-for="(item, index) in msg" :key="index">
            <Posts :msg="item"></Posts>
          </div>
        </div>
      </vueScroll>
    </div>
  </div>
</template>

<style scoped lang="sass">
@import "./../../public/sass/_sass/_mixin.sass"
#Cooperation
  height: 100%
  // background: linear-gradient(155deg, #f6d365 0%, #fda085 100%)
  background: linear-gradient(155deg, #ebbba7 0%, #fcf7f8 100%)
  // background: linear-gradient(155deg, #abecd6 0%, #fbed96 100%)
  // background: linear-gradient(155deg, #f3e7e9 0%, #e3eeff 100%)
  padding: 10px 15px 0
  position: relative
  .parent-dom
    width: 100%
    height: 100%
</style>

<script lang="ts">
import Vue from 'vue';
import vueScroll from 'vuescroll'
import Posts from '@/components/Posts.vue';

export default Vue.extend({
  name: 'Cooperation',
  components: {
    vueScroll,
    Posts
  },
  data(){
    return{
      msg: [
        {
          id: 1,
          top: true,
          src: './img/img1.webp',
          title: '中国裁判文书网使用教程',
          cont: '教你查询渣男是否有公开的法院裁判文书（部分裁判文书不公开）'
        },
        {
          id: 2,
          top: false,
          src: './img/img1.webp',
          title: '中国裁判文书网使用教程',
          cont: '教你查询渣男是否有公开的法院裁判文书（部分裁判文书不公开）'
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
