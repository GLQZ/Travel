<template>
  <div>
    <div class="item"
         v-for="(item, index) in list"
         :key="index"
    >
      <div class="item-title border-bottom">
        <span class="iconfont icon-title-icon">&#xe621;</span>
        {{item.title}}
      </div>
      <div v-if="item.children" class="item-children">
        <detail-list :list="item.children"></detail-list>
      </div>
    </div>
  </div>
</template>

<script type="text/ecmascript-6">
export default {
  name: 'DetailList',
  props: {
    list: Array
  }
}
</script>

<style scoped lang="stylus" rel="stylesheet/stylus">
  @import "~styles/varibles.styl"
  .item-title
    line-height .8rem
    font-size .32rem
    padding 0 .2rem
    .icon-title-icon
      color $bgColor
      font-size .25rem
  .item-children
    padding 0 .2rem
</style>
