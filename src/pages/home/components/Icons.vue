<template>
  <div class = "icons">
    <div class = "icon">
      <div class="icon-img">
        <img class = "icon-img-content" src="https://via.placeholder.com/100x100/">
        <p class = "icon-desc">xxxx</p>
      </div>
    </div>
        <div class = "icon">
      <div class="icon-img">
        <img class = "icon-img-content" src="https://via.placeholder.com/100x100/">
        <p class = "icon-desc">xxxx</p>
      </div>
    </div>
        <div class = "icon">
      <div class="icon-img">
        <img class = "icon-img-content" src="https://via.placeholder.com/100x100/">
        <p class = "icon-desc">xxxx</p>
      </div>
    </div>
    <div class = "icon">
      <div class="icon-img">
        <img class = "icon-img-content" src="https://via.placeholder.com/100x100/">
        <p class = "icon-desc">xxxx</p>
      </div>
    </div>
        <div class = "icon">
      <div class="icon-img">
        <img class = "icon-img-content" src="https://via.placeholder.com/100x100/">
        <p class = "icon-desc">xxxx</p>
      </div>
    </div>
        <div class = "icon">
      <div class="icon-img">
        <img class = "icon-img-content" src="https://via.placeholder.com/100x100/">
        <p class = "icon-desc">xxxx</p>
      </div>
    </div>
        <div class = "icon">
      <div class="icon-img">
        <img class = "icon-img-content" src="https://via.placeholder.com/100x100/">
        <p class = "icon-desc">xxxx</p>
      </div>
    </div>
        <div class = "icon">
      <div class="icon-img">
        <img class = "icon-img-content" src="https://via.placeholder.com/100x100/">
        <p class = "icon-desc">xxxx</p>
      </div>
    </div>

  </div>
</template>

<script>
export default {
  name: 'HomeIcons'
}
</script>

<style lang = "stylus" scoped>
  @import '~styles/variables.styl'
  .icons
    overflow hidden
    height 0
    padding-bottom 50%
    .icon
      position relative
      overflow hidden
      float left
      height 0
      width 25%
      padding-bottom 25%
      .icon-img
        position absolute
        box-sizing border-box
        padding .1rem
        top:0
        right:0
        left:0
        bottom:0.44rem
        .icon-img-content
          display block
          margin 0 auto
          height 100%
      .icon-desc
        text-align:center
        position absolute
        right:0
        left:0
        bottom:0
        height 0.44rem
        line-height 0.44rem
        color $darkTextColor
</style>
