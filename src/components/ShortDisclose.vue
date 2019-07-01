<template>
  <div>
    <ul id="shortDisclose">
      <li v-for="(item,index) of msgArr" :key="index">
        <div class="tips">
          <label v-for="(item2,index2) of item.label" :key="index2">
            <span v-if="item2.type === 1" :style="`background: rgba(0,0,0,${item2.hot * 0.1});color:#fff`">致死</span>
            <span v-else-if="item2.type === 2" :style="`background: rgba(48, 57, 82,${item2.hot * 0.1});color:${item2.hot > 5 ? '#fff' : '#000'}`">吸毒</span>
            <span v-else-if="item2.type === 3" :style="`background: rgba(45, 29, 128,${item2.hot * 0.1});color:${item2.hot > 5 ? '#fff' : '#000'}`">抢劫</span>
            <span v-else-if="item2.type === 4" :style="`background: rgba(89, 98, 117,${item2.hot * 0.1});color:${item2.hot > 5 ? '#fff' : '#000'}`">强奸</span>
            <span v-else-if="item2.type === 5" :style="`background: rgba(130, 111, 0,${item2.hot * 0.1});color:${item2.hot > 5 ? '#fff' : '#000'}`">盗窃</span>
            <span v-else-if="item2.type === 6" :style="`background: rgba(255, 177, 14,${item2.hot * 0.1});color:${item2.hot > 5 ? '#fff' : '#000'}`">猥亵</span>
            <span v-else-if="item2.type === 7" :style="`background: rgba(0, 176, 115,${item2.hot * 0.1});color:${item2.hot > 5 ? '#fff' : '#000'}`">恋童</span>
            <span v-else-if="item2.type === 8" :style="`background: rgba(0, 143, 164,${item2.hot * 0.1});color:${item2.hot > 5 ? '#fff' : '#000'}`">跟踪</span>
            <span v-else-if="item2.type === 9" :style="`background: rgba(200, 137, 137,${item2.hot * 0.1});color:${item2.hot > 5 ? '#fff' : '#000'}`">偷拍</span>
            <span v-else-if="item2.type === 10" :style="`background: rgba(196, 69, 105,${item2.hot * 0.1});color:${item2.hot > 5 ? '#fff' : '#000'}`">PUA</span>
            <span v-else-if="item2.type === 11" :style="`background: rgba(255, 0, 0,${item2.hot * 0.1});color:${item2.hot > 5 ? '#fff' : '#000'}`">家暴</span>
            <span v-else-if="item2.type === 12" :style="`background: rgba(247, 166, 77,${item2.hot * 0.1});color:${item2.hot > 5 ? '#fff' : '#000'}`">网贷</span>
            <span v-else-if="item2.type === 13" :style="`background: rgba(230, 103, 103,${item2.hot * 0.1});color:${item2.hot > 5 ? '#fff' : '#000'}`">囚禁</span>
            <span v-else-if="item2.type === 14" :style="`background: rgba(247, 143, 179,${item2.hot * 0.1});color:${item2.hot > 5 ? '#fff' : '#000'}`">淫乱</span>
            <span v-else-if="item2.type === 15" :style="`background: rgba(119, 139, 235,${item2.hot * 0.1});color:${item2.hot > 5 ? '#fff' : '#000'}`">骗婚</span>
            <span v-else-if="item2.type === 16" :style="`background: rgba(231, 127, 103,${item2.hot * 0.1});color:${item2.hot > 5 ? '#fff' : '#000'}`">偏执</span>
            <span v-else-if="item2.type === 17" :style="`background: rgba(84, 109, 229,${item2.hot * 0.1});color:${item2.hot > 5 ? '#fff' : '#000'}`">同妻</span>
            <span v-else-if="item2.type === 18" :style="`background: rgba(241, 144, 102,${item2.hot * 0.1});color:${item2.hot > 5 ? '#fff' : '#000'}`">诈骗</span>
            <span v-else-if="item2.type === 19" :style="`background: rgba(0, 185, 7,${item2.hot * 0.1});color:${item2.hot > 5 ? '#fff' : '#000'}`">艾滋</span>
            <span v-else-if="item2.type === 20" :style="`background: rgba(164, 164, 164,${item2.hot * 0.1});color:${item2.hot > 5 ? '#fff' : '#000'}`">其他</span>
            <span v-else v-show="false">标签不存在</span>
          </label>
        </div>
        <div class="people">
          <p>{{item.name}}、{{item.age}}岁</p>
          <p>学历：{{item.education}}</p>
          <p>活动范围：{{item.place}}</p>
        </div>
        <div class="people-sex">
          <svg class="icon" aria-hidden="true"><use :xlink:href="`#icon-${item.sex === 1 ? 'nanshen' : 'nvren'}`"></use></svg>
        </div>
        <div class="describe">
          {{item.describe}}
        </div>
      </li>
    </ul>
  </div>
</template>

<script lang="ts">
import Vue from 'vue';

export default Vue.extend({
  name: 'HelloWorld',
  props: {
    msg: String,
  },
  data(){
    return{
      msgArr: [
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
      ]
    }
  }
});
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="sass">
@import "./../../public/sass/_sass/_mixin.sass"
#shortDisclose
  @include _wh(100%,auto)
  li
    background: #fff
    border-radius: 10px
    padding: 10px
    margin-bottom: 10px
    position: relative
    .tips
      @include _flex(flex-start)
      flex-wrap: wrap
      label
        width: 20%
        display: flex
        margin-bottom: 3px
        text-align: center
        span
          width: 80%
          line-height: 1.5
          margin: 0 auto
          border-radius: 3px
    .people
      p
        font-size: 12px
        white-space: nowrap
        line-height: 1.5
        color: #5f5f5f
    .people-sex
      @include _wh(30px)
      font-size: 17px
      text-align: center
      @include _position(0,auto)
      @include _border(2px,solid,#000,0 10px 0 10px)
      background: #efefef
      right: 0
    .describe
      margin-top: 5px
      padding-top: 7px
      color: #5d5d5d
      border-top: 1px dotted #000
</style>
