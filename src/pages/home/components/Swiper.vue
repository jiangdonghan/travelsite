<template>
  <div class = "wrapper">
    <swiper :options="swiperOption">
      <!-- slides -->
      <swiper-slide v-for="item of swiperList" :key = item.id>
        <img class = "swiper-img" :src="item.imgUrl">
      </swiper-slide>

      <!-- Optional controls -->
      <div class="swiper-pagination" slot="pagination"></div>
    </swiper>
  </div>

</template>

<script>
export default {
  name: 'HomeSwiper',
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true
      },
      swiperList: [{
        id: '0001',
        imgUrl: 'https://via.placeholder.com/600x150/0000FF'
      },
      {
        id: '0002',
        imgUrl: 'https://via.placeholder.com/600x150/'
      }
      ]
    }
  }
}

</script>

<style lang="stylus" scoped>
  .wrapper >>> .swiper-pagination-bullet-active
    background #fff
  .wrapper
    width 100%
    overflow hidden
    height 0
    padding-bottom 25%
    background #eee
    // or height:31.25vw
    .swiper-img
      width 100%

</style>
