<template>
  <div class="header">
    <div class="header-left">
      <div class="iconfont icon-return">&#xe6d8;</div>
    </div>
    <div class="header-middle">
      <span class="iconfont icon-search">&#xe600;</span>
      城市/景点/主题
    </div>
    <router-link to="/city">
      <div class="header-right">
        {{this.city}}
        <span class="iconfont icon-arrow">&#xe662;</span>
      </div>
    </router-link>
  </div>
</template>

<script type="text/ecmascript-6">
export default {
  name: 'HomeHeader',
  props: {
    city: String
  }
}
</script>

<style scoped lang="stylus" rel="stylesheet/stylus">
  @import "~styles/varibles.styl"
  .header
    display flex
    height $headerHeight
    background $bgColor
    color #fff
    line-height $headerHeight
    .header-left
      width .64rem
      float left
      .icon-return
        text-align center
        font-size .4rem
    .header-middle
      flex 1
      height .62rem
      line-height .62rem
      margin-top .12rem
      margin-left .2rem
      background #fff
      border-radius .1rem
      padding-left .2rem
      color #ccc
    .header-right
      color #fff
      width 1.24rem
      float right
      text-align center
      .icon-arrow
        margin-left -.1rem
        font-size .3rem
</style>
