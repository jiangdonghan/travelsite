<template>
  <div class="header">
    城市选择
    <router-link to="/">
    <div class="iconfont header-back">&#xe624;</div>
    </router-link>
  </div>
</template>
<script>
export default {
  name: 'CityHeader'
}
</script>

<style lang="stylus" scoped>
  @import '~styles/variables.styl'
  .header
    position relative
    overflow: hidden
    height: 0.86rem
    line-height: 0.86rem
    text-align: center
    color #fff
    background: $bgColor
    font-size .32rem
    .header-back
      color #fff
      position absolute
      top 0
      left 0
      width .64rem
      text-align center
      font-size .4rem
</style>
