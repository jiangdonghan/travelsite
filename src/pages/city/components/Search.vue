<template>
<div>
  <div class="search">
    <input v-model="keyword" class="search-input" type="text" placeholder="Type city name"/>
  </div>
  <div class="search-content" v-show="keyword" ref="search">
    <ul>
      <li class="search-item border-bottom" v-for="item of list" :key="item.id"
      @click="handleCityClick(item.name)">{{item.name}}
      </li>
      <li class="search-item border-bottom" v-show="hasNoList">No found</li>
    </ul>
  </div>
</div>
</template>
<script>
import { mapMutations } from 'vuex'
import Bscroll from 'better-scroll'
export default {
  name: 'CitySearch',
  props: {
    cities: Object
  },
  data () {
    return {
      keyword: '',
      list: [],
      timer: null
    }
  },
  computed: {
    hasNoList () {
      return !this.list.length
    }
  },
  methods: {
    handleCityClick (city) {
      this.changeCity(city)
      this.$router.push('/')
    },
    ...mapMutations(['changeCity'])
  },
  watch: {
    keyword () {
      if (this.timer) {
        clearTimeout(this.timer)
      }
      if (!this.keyword) {
        this.list = []
        return
      }
      this.timer = setTimeout(() => {
        const result = []
        for (let i in this.cities) {
          this.cities[i].forEach((value) => {
            if (value.spell.indexOf(this.keyword) > -1 || value.name.indexOf(this.keyword) > -1) {
              result.push(value)
            }
          })
        }
        this.list = result
      }, 100)
    }
  },
  mounted () {
    this.scroll = new Bscroll(this.$refs.search, {click: true})
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/variables.styl'
  .search
    height: .72rem
    background: $bgColor
    padding 0 0.1rem
    .search-input
      box-sizing border-box
      width 100%
      height .62rem
      line-height .62rem
      text-align center
      border-radius .06rem
      color #666
      padding 0 .1rem
  .search-content
    z-index 1
    overflow hidden
    background #eee
    position absolute
    top 1.58rem
    left 0
    right 0
    bottom 0
    .search-item
      line-height .62rem
      padding-left .2rem
      color #666
      background #fff
</style>
