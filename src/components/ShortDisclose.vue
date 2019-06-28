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
          <label>{{item.name}}</label>
          <label>{{item.sex === 1 ? '男' : '女'}}</label>
          <label>{{item.age}}</label>
          <label>{{item.place}}</label>
          <label>{{item.education}}</label>
        </div>
        {{item.describe}}
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
          label: [
            {type: 10, hot: 10}, // 无解，纯黑，不解释，最高犯罪
            {type: 9, hot: 10},
          ],
          name: '陈某熙',
          sex: 1,
          age: 24,
          place: '北京三里屯',
          education: '北京外国语学院',
          describe: '身高178cm左右，右手腕有痣，喜欢打王者荣耀，养有一只加菲。'
        }
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
    label
      font-size: 12px
      white-space: nowrap
</style>
