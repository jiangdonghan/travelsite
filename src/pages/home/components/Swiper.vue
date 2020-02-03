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
        imgUrl: 'https://images.pexels.com/photos/1619854/pexels-photo-1619854.jpeg?auto=compress&cs=tinysrgb&dpr=1&w=500'
      },
      {
        id: '0002',
        imgUrl: 'https://images.pexels.com/photos/2846069/pexels-photo-2846069.jpeg?auto=compress&cs=tinysrgb&dpr=1&w=500'
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
    padding-bottom 35%
    background #eee
    // or height:31.25vw
    .swiper-img
      width 100%
      height 35vw
</style>
