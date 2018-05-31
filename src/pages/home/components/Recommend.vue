<template>
  <div>
    <div class="title">猜你喜欢</div>
    <ul>
      <li class="item border-bottom" v-for="item in recommendList" :key="item.id">
        <img class="item-img" :src="item.imgUrl" alt="Loading">
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
          <button class="item-button">查看详情</button>
        </div>
      </li>
    </ul>
  </div>
</template>

<script type="text/ecmascript-6">
export default {
  name: 'HomeRecommend',
  data () {
    return {
      recommendList: [{
        id: '0001',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1607/6c/6ce376cd5775ce6fb4.img.jpg_200x200_7ed7ce79.jpg',
        title: '棕榈谷水城',
        desc: '反正我没去过那就说明一般哈哈哈'
      }, {
        id: '0002',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1607/6c/6ce376cd5775ce6fb4.img.jpg_200x200_7ed7ce79.jpg',
        title: '棕榈谷水城',
        desc: '反正我没去过那就说明一般哈哈哈'
      }, {
        id: '0003',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1607/6c/6ce376cd5775ce6fb4.img.jpg_200x200_7ed7ce79.jpg',
        title: '棕榈谷水城',
        desc: '反正我没去过那就说明一般哈哈哈'
      }, {
        id: '0004',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1607/6c/6ce376cd5775ce6fb4.img.jpg_200x200_7ed7ce79.jpg',
        title: '棕榈谷水城',
        desc: '反正我没去过那就说明一般哈哈哈'
      }]
    }
  }
}
</script>

<style scoped lang="stylus" rel="stylesheet/stylus">
  @import "~styles/varibles.styl"
  @import "~styles/mixins.styl"
  .title
    margin-top .2rem
    line-height .8rem
    background #eee
    text-indent .2rem
  .item
    overflow hidden
    display flex
    height 1.9rem
    .item-img
      width 1.7rem
      height 1.7rem
      padding .1rem
    .item-info
      flex 1
      padding .1rem
      min-width 0
      .item-title
        line-height .54rem
        font-size .32rem
        ellipsis()
      .item-desc
        line-height .4rem
        color #bbb
        ellipsis()
      .item-button
        line-height .44rem
        margin-top .16rem
        background $bgColor
        padding 0 .2rem
        border-radius .1rem
        color #fff
</style>
