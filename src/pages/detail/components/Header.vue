<template>
<div>
  <router-link tag="div" to="/" class="header-abs" v-show="showAbs">
    <div class="iconfont back-icon">&#xe624;</div>
  </router-link>
  <div class="header-fixed" v-show="!showAbs" :style="opacityStyle">
    <router-link tag="div" to="/" class="iconfont header-back-icon">&#xe624;</router-link>
    景点详情
  </div>
</div>
</template>

<script>

export default {
  name: 'DetailHeader',
  data () {
    return {
      showAbs: true,
      opacityStyle: {
        opacity: 0
      }
    }
  },
  methods: {
    handleScroll () {
      const top = document.documentElement.scrollTop
      if (top > 60) {
        let opacity = top / 140
        opacity = opacity > 1 ? 1 : opacity
        this.opacityStyle = { opacity }
        this.showAbs = false
      } else {
        this.showAbs = true
      }
    }
  },
  // keep-alive so it will be used
  mounted () {
    window.addEventListener('scroll', this.handleScroll)
    console.log('scroll')
  },
  beforeDestroy () {
    window.removeEventListener('scroll', this.handleScroll)
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/variables.styl';
  .header-abs
    position: absolute
    left: .2rem
    top: .2rem
    width: .8rem
    height: .8rem
    border-radius .4rem
    background rgba(0,0,0,.8)
    text-align center
    line-height .8rem
    .back-icon
      color #fff
      font-size .4rem
  .header-fixed
    z-index: 2
    position fixed
    top: 0
    left: 0
    right: 0
    overflow: hidden
    height: 0.86rem
    line-height: 0.86rem
    text-align: center
    color #fff
    background: $bgColor
    font-size .32rem
    .header-back-icon
      color #fff
      position absolute
      top 0
      left 0
      width .64rem
      text-align center
      font-size .4rem
</style>
