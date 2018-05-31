<template>
<div class="wrapper">
  <swiper :options="swiperOption" v-if="showSwiper">
    <swiper-slide v-for="item in list" :key="item.id">
      <img class="swiper-img" :src="item.imgUrl" alt="Loading">
    </swiper-slide>
    <div class="swiper-pagination"  slot="pagination"></div>
  </swiper>
</div>
</template>

<script type="text/ecmascript-6">
export default {
  name: 'HomeSwiper',
  props: {
    list: Array
  },
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        autoplay: 3000,
        loop: true
      }
    }
  },
  computed: {
    showSwiper () {
      return this.list.length
    }
  }
}
</script>

<style scoped lang="stylus" rel="stylesheet/stylus">
  @import "~styles/varibles.styl"
  .wrapper >>> .swiper-pagination-bullet-active
    background #fff !important
  .wrapper
    width 100%
    height 0
    overflow hidden
    padding-bottom 30.3%
    background #eee
    .swiper-img
      width 100%
</style>
