<template>
    <div class="header">
        <div class="header-left">icon1</div>
        <div class="header-input">city/tourist attractions/theme</div>
        <div class="header-right">dropdown</div>
    </div>
</template>
<script>
export default {
  name: 'HomeHeader'
}
</script>
<style lang="stylus" scoped>
    .header
        display: flex
        line-height: .86rem
        background : #00bcd4
        color: #fff
        .header-left
            width: .64rem
            float: left
        .header-input
            flex:1
            background: #fff
            border-radius: .1rem
            margin-top: .12rem
            margin-left .2rem
            line-height :.64rem
            height .64rem
            color #ccc
        .header-right
            width: 1.24rem
            float: right
            text-align center
</style>
