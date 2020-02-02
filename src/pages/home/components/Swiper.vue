<template>
  <div class = "wrapper">
    <swiper :options="swiperOption">
      <!-- slides -->
      <swiper-slide>
        <img class = "swiper-img" src="https://via.placeholder.com/600x150/0000FF">
      </swiper-slide>
      <swiper-slide>
        <img class = "swiper-img" src="https://via.placeholder.com/600x150/">
      </swiper-slide>
      <!-- Optional controls -->
      <div class="swiper-pagination" slot="pagination"></div>
    </swiper>
  </div>

</template>

<script>
  export default {
    name: 'HomeSwiper',
    data() {
      return {
        swiperOption: {}
      }
    }
  }

</script>

<style lang="stylus" scoped>
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
