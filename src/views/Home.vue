<template>
  <div id="home">
    <ShortDisclose msg="实时滚动的短料"/>
  </div>
</template>

<style lang="sass">
#home
  height: 100%
  padding: 10px 15px
  background: linear-gradient(155deg, #a8edea 0%, #fed6e3 100%)
</style>

<script lang="ts">
import Vue from 'vue';
import ShortDisclose from '@/components/ShortDisclose.vue';

export default Vue.extend({
  name: 'home',
  components: {
    ShortDisclose,
  },
});
</script>
