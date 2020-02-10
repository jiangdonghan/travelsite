<template>
  <ul class="list">
    <li class="item" v-for="(item,key) of alphabet" :key="key">{{key}}</li>
  </ul>
</template>
<script>
export default {
  name: 'CityAlphabet',
  props: {
    alphabet: Object
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/variables.styl'
  .list
    display flex
    flex-direction column
    justify-content center
    position absolute
    right 0
    bottom 0
    top 1.58rem
    width .4rem
    .item
      text-align center
      line-height .4rem
      color $bgColor
</style>
