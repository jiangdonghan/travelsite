<template>
  <div>
    <div class = "title">Recommendations</div>

    <ul>
      <li class = "item border-bottom" v-for="item of recommendList" :key="item.id">
        <img  class="item-img" :src="item.imgUrl"/>
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
          <button class="item-button">Description</button>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeRecommend',
  data () {
    return {
      recommendList: [{
        id: '0001',
        imgUrl: 'https://imgs.qunarzz.com/sight/p0/1501/18/181cff1e8af11041.water.jpg_200x200_2e185c41.jpg',
        title: '悉尼海洋世界',
        desc: '浪漫悉尼首站，浪漫的海洋主题乐园'
      }, {
        id: '0002',
        imgUrl: 'https://imgs.qunarzz.com/sight/p0/1903/b0/b0a81289b537c934a3.water.jpg_200x200_816c0f59.jpg',
        title: '澳门塔蹦级',
        desc: '澳门塔蹦极'
      }, {
        id: '0003',
        imgUrl: 'https://imgs.qunarzz.com/sight/p0/1410/16/f0e5b7624c03a47238d108469d8a58e6.jpg_200x200_05bd1651.jpg',
        title: 'shopping mall',
        desc: 'hongkong shopping mall'
      }
      ]
    }
  }
}
</script>

<style lang = "stylus" scoped>
@import '~styles/mixins.styl';
  .title
    margin-top .2rem
    line-height: .8rem
    background: #eee
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
        color #ccc
        ellipsis()
      .item-button
        line-height .44rem
        margin-top .16rem
        background #ff9300
        padding 0 .2rem
        border-radius 0.06rem
        color #fff
</style>
