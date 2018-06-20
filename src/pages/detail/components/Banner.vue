<template>
  <div>
    <div class="banner" @click="handleBannerClick">
      <img
        class="banner-img"
        src="//img1.qunarzz.com/sight/p0/1409/19/adca619faaab0898245dc4ec482b5722.jpg_600x330_f922b488.jpg"
        alt="Loading">
      <div class="banner-info">
        <div class="banner-title">故宫(AAAAA景区)</div>
        <div class="banner-map">
          <span class="iconfont banner-icon icon-map">&#xe618;</span>
          20
        </div>
      </div>
    </div>
    <common-gallery
      :imgs="imgs"
      v-show="showGallery"
      @close="handleGalleryClose"
    ></common-gallery>
  </div>
</template>

<script type="text/ecmascript-6">
import CommonGallery from 'common/gallery/Gallery'
export default {
  name: 'DetailBanner',
  data () {
    return {
      showGallery: false,
      imgs: ['http://img1.qunarzz.com/sight/p0/1410/9d/fe8109ab5df1c9c324e74284fa802e72.water.jpg_r_800x800_b9a5440a.jpg',
        'http://img1.qunarzz.com/sight/p0/1410/9d/fe8109ab5df1c9c324e74284fa802e72.water.jpg_r_800x800_b9a5440a.jpg']
    }
  },
  methods: {
    handleBannerClick () {
      this.showGallery = true
    },
    handleGalleryClose () {
      this.showGallery = false
    }
  },
  components: {
    CommonGallery
  }
}
</script>

<style scoped lang="stylus" rel="stylesheet/stylus">
  @import "~styles/varibles.styl"
  .banner
    position relative
    overflow hidden
    height 0
    padding-bottom 55%
    .banner-img
      width 100%
    .banner-info
      color #fff
      display flex
      position absolute
      left 0
      right 0
      bottom 0
      line-height .6rem
      background-image linear-gradient(top, rgba(0,0,0,0), rgba(0,0,0,.8))
      .banner-title
        flex 1
        font-size .32rem
        padding 0 .2rem
      .banner-map
        line-height .32rem
        height .32rem
        margin-top .14rem
        padding 0 .4rem
        border-radius .2rem
        background rgba(0,0,0,.8)
        font-size .24rem
        .banner-icon
          font-size .24rem
</style>
