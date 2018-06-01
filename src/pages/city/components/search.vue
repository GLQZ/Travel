<template>
  <div class="search">
    <input class="search-input" type="text" placeholder="输入城市名或拼音">
  </div>
</template>

<script type="text/ecmascript-6">
export default {
  name: 'CitySearcg'
}
</script>

<style scoped lang="stylus" rel="stylesheet/stylus">
  @import "~styles/varibles.styl"
  .search
    height .72rem
    background $bgColor
    padding 0 .1rem
    .search-input
      box-sizing border-box
      padding 0 .2rem
      height .62rem
      line-height .62rem
      width 100%
      text-align center
      border-radius .06rem
      color #666
</style>
