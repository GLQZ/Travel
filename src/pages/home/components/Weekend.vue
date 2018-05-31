<template>
  <div>
    <div class="title">周末去哪儿</div>
    <ul>
      <li class="item border-bottom" v-for="item in recommendList" :key="item.id">
        <div class="item-img-wrapper">
          <img class="item-img" :src="item.imgUrl" alt="Loading">
        </div>
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
        </div>
      </li>
    </ul>
  </div>
</template>

<script type="text/ecmascript-6">
export default {
  name: 'HomeWeekend',
  data () {
    return {
      recommendList: [{
        id: '0001',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1505/4b/d04aa63b1b0ab3.jpg_r_640x214_a3a9c5b6.jpg',
        title: '东莞必游Top10',
        desc: '东莞，同住一座城，不需要理由'
      }, {
        id: '0002',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1505/4b/d04aa63b1b0ab3.jpg_r_640x214_a3a9c5b6.jpg',
        title: '东莞必游Top10',
        desc: '东莞，同住一座城，不需要理由'
      }, {
        id: '0003',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1505/4b/d04aa63b1b0ab3.jpg_r_640x214_a3a9c5b6.jpg',
        title: '东莞必游Top10',
        desc: '东莞，同住一座城，不需要理由'
      }, {
        id: '0004',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1505/4b/d04aa63b1b0ab3.jpg_r_640x214_a3a9c5b6.jpg',
        title: '东莞必游Top10',
        desc: '东莞，同住一座城，不需要理由'
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
  .item-img-wrapper
    overflow hidden
    height 0
    padding-bottom 33.9%
    .item-img
      width 100%
  .item-info
    padding .1rem
    .item-title
      line-height .54rem
      font-size .32rem
      ellipsis()
    .item-desc
      line-height .4rem
      color #bbb
      ellipsis()
</style>
