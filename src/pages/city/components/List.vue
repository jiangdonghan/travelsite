<template>
<div class = "list">
  <div class="area">
    <div class="title border-topbottom">Current City</div>
    <div class="button-list">
      <div class="button-wrapper">
      <div class="button">button</div>
      </div>
    </div>
  </div>
     <div class="area">
    <div class="title border-topbottom">Hot City</div>
    <div class="button-list">
      <div class="button-wrapper">
      <div class="button">北京</div>
      </div>
      <div class="button-wrapper">
      <div class="button">上海</div>
      </div>
      <div class="button-wrapper">
      <div class="button">xx</div>
      </div>
      <div class="button-wrapper">
      <div class="button">xx</div>
      </div>
      <div class="button-wrapper">
      <div class="button">xx</div>
      </div>
    </div>
  </div>
  <div class="area">
    <div class="title border-topbottom">A</div>
    <div class="item-list">
      <div class="item border-bottom">acity</div>
      <div class="item border-bottom">acity</div>
      <div class="item border-bottom">acity</div>
      <div class="item border-bottom">acity</div>
      <div class="item border-bottom">acity</div>
      <div class="item border-bottom">acity</div>
    </div>
    <div class="title border-topbottom">B</div>
    <div class="item-list">
      <div class="item border-bottom">acity</div>
      <div class="item border-bottom">acity</div>
      <div class="item border-bottom">acity</div>
      <div class="item border-bottom">acity</div>
      <div class="item border-bottom">acity</div>
      <div class="item border-bottom">acity</div>
    </div>
    <div class="title border-topbottom">C</div>
    <div class="item-list">
      <div class="item border-bottom">acity</div>
      <div class="item border-bottom">acity</div>
      <div class="item border-bottom">acity</div>
      <div class="item border-bottom">acity</div>
      <div class="item border-bottom">acity</div>
      <div class="item border-bottom">acity</div>
    </div>
    <div class="title border-topbottom">D</div>
    <div class="item-list">
      <div class="item border-bottom">acity</div>
      <div class="item border-bottom">acity</div>
      <div class="item border-bottom">acity</div>
      <div class="item border-bottom">acity</div>
      <div class="item border-bottom">acity</div>
      <div class="item border-bottom">acity</div>
    </div>
    <div class="title border-topbottom">E</div>
    <div class="item-list">
      <div class="item border-bottom">acity</div>
      <div class="item border-bottom">acity</div>
      <div class="item border-bottom">acity</div>
      <div class="item border-bottom">acity</div>
      <div class="item border-bottom">acity</div>
      <div class="item border-bottom">acity</div>
    </div>
    <div class="title border-topbottom">F</div>
    <div class="item-list">
      <div class="item border-bottom">acity</div>
      <div class="item border-bottom">acity</div>
      <div class="item border-bottom">acity</div>
      <div class="item border-bottom">acity</div>
      <div class="item border-bottom">acity</div>
      <div class="item border-bottom">acity</div>
    </div>
  </div>
</div>
</template>
<script>
export default {
  name: 'CityList'
}
</script>

<style lang="stylus" scoped>
  @import '~styles/variables.styl'
  .border-topbottom
    &:before
      border-color: #ccc
    &:after
      border-color: #ccc
  .border-bottom
    &:before
      border-color: #ccc
  .list
    overflow hidden
    position absolute
    top 1.58rem
    left 0
    bottom 0
    right 0
    background red
    .title
      line-height .4rem
      background #eee
      padding-left .2rem
      color #666
    .button-list
      padding .1rem .6rem .1rem .1rem
      overflow hidden
      .button-wrapper
        float: left
        width 33.33%
        .button
          padding .1rem 0
          text-align center
          margin .1rem
          border .02rem solid #ccc
          border-radius .06rem
    .item-list
      .item
        line-height .76rem
        color #666
        padding-left .2rem
</style>
