<template>
  <div>
    <div class = "title">Weekend</div>

    <ul>
      <li class = "item border-bottom" v-for="item of recommendList" :key="item.id">
        <div class="item-img-wrapper"><img  class="item-img" :src="item.imgUrl"/></div>
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
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
        imgUrl: 'https://imgs.qunarzz.com/sight/source/1811/f3/86173f863bef61.jpg_r_640x214_52b003ac.jpg',
        title: '悉尼海洋世界',
        desc: '浪漫悉尼首站，浪漫的海洋主题乐园'
      }, {
        id: '0002',
        imgUrl: 'https://imgs.qunarzz.com/sight/source/1510/6e/1ea71e2f04e.jpg_r_640x214_aa6f091d.jpg',
        title: '澳门塔蹦级',
        desc: '澳门塔蹦极'
      }, {
        id: '0003',
        imgUrl: 'https://imgs.qunarzz.com/sight/source/1505/9e/21df651e19af5d.jpg_r_640x214_3ea5bb38.jpg',
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
    line-height: .8rem
    background: #eee
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
      color #ccc
      ellipsis()
</style>
