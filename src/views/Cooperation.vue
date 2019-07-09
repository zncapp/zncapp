<template>
  <div id="Cooperation">
    <div class="parent-dom">
      <vueScroll :ops="ops">
        <div class="child-dom">
          <div class="item">
            <img src="./../../public/img/img1.webp"/>
            <strong>中国裁判文书网使用教程</strong>
            <p>教你查询渣男是否有公开的法院裁判文书（部分裁判文书不公开）</p>
          </div>
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
          time: '2019-03-05',
          title: '如何使用天眼查，查询公司经营状况',
          cont: '天眼查分为免费查询与收费查询，每个注册账号每天拥有3次免费查询的机会。由于是免费版缘故，部分查询资料受限。需要付费查找。然而付费查找可以通过在淘宝上购买VIP账号，进行短暂的一次性查询。'
        },
        {
          id: 2,
          top: false,
          time: '2019-03-05',
          title: '如何查询法人的公司经营状况',
          cont: '百度搜索：“国家企业信用信息公示系统”，选择域名结尾为：“gov.cn”的网址。知晓企业的全称，即可查询到该企业的经营状况。'
        },
        {
          id: 3,
          top: false,
          time: '2019-03-05',
          title: '如何查询公开的在逃嫌疑犯教程',
          cont: '由于没有整合的网站，只有在当地警局的网站查询最新资料。注意更新。'
        },
        {
          id: 4,
          top: false,
          time: '2019-03-05',
          title: '中央信网办-违法和不良信息举报中心使用教程',
          cont: '由于没有整合的网站，只有在当地警局的网站查询最新资料。注意更新。'
        },
        {
          id: 5,
          top: false,
          time: '2019-03-05',
          title: '全国12315互联网平台-工商举报-使用教程',
          cont: '国家工商总局升级12315:可用支付宝一键投诉。'
        },
        {
          id: 5,
          top: false,
          time: '2019-03-05',
          title: '全国12315互联网平台-工商举报-使用教程',
          cont: '国家工商总局升级12315:可用支付宝一键投诉。'
        },
        {
          id: 6,
          top: false,
          time: '2019-03-05',
          title: '为什么中国男人选择去泰国杀媳妇？',
          cont: '泰国的法律对外来的犯人并不宽容。'
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
