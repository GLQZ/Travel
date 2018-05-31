<template>
  <div class="header">
    城市选择
    <router-link to="/">
      <div class="iconfont icon-return">&#xe6d8;</div>
    </router-link>
  </div>
</template>

<script type="text/ecmascript-6">
export default {
  name: 'CityHeader'
}
</script>

<style scoped lang="stylus" rel="stylesheet/stylus">
  @import "~styles/varibles.styl"
  .header
    overflow hidden
    position relative
    height $headerHeight
    line-height $headerHeight
    text-align center
    color #fff
    background $bgColor
    font-size .32rem
    .icon-return
      position absolute
      font-size .4rem
      text-align center
      top 0
      left 0
      width .64rem
      color #fff
</style>
