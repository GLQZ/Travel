<template>
  <div>
    <div class="banner" @click="handleBannerClick">
      <img
        class="banner-img"
        :src="bannerImg"
        alt="Loading">
      <div class="banner-info">
        <div class="banner-title">{{this.sightName}}</div>
        <div class="banner-map">
          <span class="iconfont banner-icon icon-map">&#xe618;</span>
          {{this.sightName.length}}
        </div>
      </div>
    </div>
    <fade-animation>
      <common-gallery
        :imgs="gallaryImgs"
        v-show="showGallery"
        @close="handleGalleryClose"
      ></common-gallery>
    </fade-animation>
  </div>
</template>

<script type="text/ecmascript-6">
import CommonGallery from 'common/gallery/Gallery'
import FadeAnimation from 'common/fade/FadeAnimation'
export default {
  name: 'DetailBanner',
  data () {
    return {
      showGallery: false
    }
  },
  props: {
    sightName: String,
    bannerImg: String,
    gallaryImgs: Array
  },
  components: {
    CommonGallery,
    FadeAnimation
  },
  methods: {
    handleBannerClick () {
      this.showGallery = true
    },
    handleGalleryClose () {
      this.showGallery = false
    }
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
