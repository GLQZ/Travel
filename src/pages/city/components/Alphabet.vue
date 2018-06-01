<template>
  <ul class="list">
    <li class="item">a</li>
    <li class="item">a</li>
    <li class="item">a</li>
    <li class="item">a</li>
    <li class="item">a</li>
  </ul>
</template>

<script type="text/ecmascript-6">
export default {
  name: 'CityAlphabet'
}
</script>

<style scoped lang="stylus" rel="stylesheet/stylus">
  @import "~styles/varibles.styl"
  .list
    display flex
    flex-direction column
    justify-content center
    position absolute
    top 1.58rem
    right 0
    bottom 0
    width 1.5em
    .item
      line-height .4rem
      text-align center
      color $bgColor
</style>
