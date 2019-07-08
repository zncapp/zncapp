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
          src: './img/img2.png',
          name: '林*康',
          title: '武汉雄楚大道楚平路',
          cont: '6月26号晚上7点多我从雄楚大道楚平路的brt地下通道口快走出地面时，他从我背后狠狠抓了一把我的屁股，手直接伸进裙子里面抓了隐私部位。我惊叫一声，只见他从我身边笑嘻嘻快速走过，我立刻愤怒地追上去拍他后背叫住他，跟他理论，他立刻骂我神经病，并企图快速通过brt入口。当时周围并无他人，我立刻向brt入口工作人员求救，好在工作人员非常迅速地将他拉回并控制住（感谢），随后支持我报警。'
        },
        {
          id: 2,
          top: false,
          src: './img/img2.png',
          name: '林*康',
          title: '武汉雄楚大道楚平路',
          cont: '6月26号晚上7点多我从雄楚大道楚平路的brt地下通道口快走出地面时，他从我背后狠狠抓了一把我的屁股，手直接伸进裙子里面抓了隐私部位。我惊叫一声，只见他从我身边笑嘻嘻快速走过，我立刻愤怒地追上去拍他后背叫住他，跟他理论，他立刻骂我神经病，并企图快速通过brt入口。当时周围并无他人，我立刻向brt入口工作人员求救，好在工作人员非常迅速地将他拉回并控制住（感谢），随后支持我报警。'
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