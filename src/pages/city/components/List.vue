<template>
<div class = "list" ref="wrapper">
  <div>
  <div class="area">
    <div class="title border-topbottom">Current City</div>
    <div class="button-list">
      <div class="button-wrapper">
      <div class="button">{{this.currrentCity}}</div>
      </div>
    </div>
  </div>
     <div class="area">
    <div class="title border-topbottom">Hot City</div>
    <div class="button-list">
      <div class="button-wrapper" v-for="item of hot" :key="item.id" @click="handleCityClick(item.name)">
      <div class="button">{{item.name}}</div>
      </div>
    </div>
  </div>
  <div class="area" v-for="(item, key) of cities" :key="key" :ref="key">
    <div class="title border-topbottom">{{key}}</div>
    <div class="item-list" v-for="innerItem of item" :key="innerItem.id">
      <div class="item border-bottom" @click="handleCityClick(innerItem.name)">{{innerItem.name}}</div>
    </div>
  </div>
  </div>
</div>
</template>
<script>
import { mapState, mapMutations } from 'vuex'
import Bscroll from 'better-scroll'
export default {
  name: 'CityList',
  mounted () {
    this.scroll = new Bscroll(this.$refs.wrapper, {click: true})
  },
  computed: {
    ...mapState({
      currrentCity: 'city'
    })
  },
  props: {
    hot: Array,
    cities: Object,
    letter: String
  },
  methods: {
    handleCityClick (city) {
      this.changeCity(city)
      this.$router.push('/')
    },
    ...mapMutations(['changeCity'])
  },
  watch: {
    letter () {
      if (this.letter) {
        const letter = this.letter
        const element = this.$refs[letter][0]
        this.scroll.scrollToElement(element)
      }
    }
  }
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
    .title
      line-height .54rem
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
