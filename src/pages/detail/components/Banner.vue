<template>
<div>
  <div class="banner" @click="handleBannerClick">
    <img class="banner-img" src="http://placekitten.com/600/330"/>
    <div class="banner-info">
      <div class="banner-title">Lorem, ipsum.</div>
      <div class="banner-number">
        <span class="iconfont banner-icon">&#xe662;</span>39
      </div>
    </div>
  </div>
  <common-gallery :imgs="imgs" v-show="showGallery" @close="handleGallaryClose"></common-gallery>
</div>
</template>

<script>
import CommonGallery from 'common/gallery/Gallery'
export default {
  name: 'DetailBanner',
  data () {
    return {
      showGallery: false,
      imgs: ['http://placekitten.com/800/800', 'http://placekitten.com/801/800']
    }
  },
  methods: {
    handleBannerClick () {
      this.showGallery = true
    },
    handleGallaryClose () {
      this.showGallery = false
    }
  },
  components: {
    CommonGallery
  }
}
</script>

<style lang="stylus" scoped>
  .banner
    position relative
    overflow hidden
    height 0
    padding-bottom 55%
    .banner-img
      width 100%
    .banner-info
      position absolute
      display flex
      left 0
      right 0
      bottom 0
      line-height .6rem
      color #fff
      background-image linear-gradient(top, rgba(0, 0, 0,0), rgba(0, 0, 0, .8))
      .banner-title
        font-size .32rem
        padding 0 .2rem
        flex 1
      .banner-number
        margin-top .14rem
        padding 0 .4rem
        line-height .32rem
        height .32rem
        border-radius .2rem
        background  rgba(0, 0, 0, .8)
        font-size .32rem
        .banner-icon
          font-size .32rem
          padding-right 0.15rem
</style>
