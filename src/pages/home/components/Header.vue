<template>
    <div class="header">
        <div class="header-left">
            <div class="iconfont back-icon">&#xe624;</div>
            </div>
        <div class="header-input">
            <span class="iconfont">&#xe632;</span>
            city/tourist attractions/theme</div>
        <router-link to="/city">
        <div class="header-right">{{this.city}}<span class="iconfont arrow-icon">&#xe62d;</span></div>
        </router-link>
    </div>
</template>
<script>
import { mapState } from 'vuex'
export default {
  name: 'HomeHeader',
  computed: {
    ...mapState(['city'])
  }
}
</script>
<style lang="stylus" scoped>
    @import '~styles/variables.styl'
    .header
        display: flex
        line-height: .86rem
        background : $bgColor
        color: #fff
        .header-left
            width: .64rem
            float: left
            .back-icon
                text-align center
                font-size .4rem
        .header-input
            flex:1
            background: #fff
            border-radius: .1rem
            margin-top: .12rem
            margin-left .2rem
            line-height :.64rem
            height .64rem
            color #ccc
            padding-left 0.2 rem
        .header-right
            min-width: 1.04rem
            padding 0 .1rem
            float: right
            text-align center
            color #fff
            .arrow-icon
                margin-left 0.1rem
                font-size 0.24rem
</style>
