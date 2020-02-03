<template>
  <div class="icons">
    <swiper :options="swiperOption">
      <swiper-slide v-for="(page,index) of pages" :key="index">
        <div class="icon" v-for="item of page"
        :key="item.id">
          <div class="icon-img">
            <img
              class="icon-img-content"
              :src='item.imgUrl'
            />
            <p class="icon-desc">{{item.desc}}</p>
          </div>
        </div>
      </swiper-slide>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeIcons',
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination'
      },
      iconList: [
        {
          id: '0001',
          imgUrl:
            '//s.qunarzz.com/homenode/images/touchheader/flight.png',
          desc: 'Flight'
        },
        {
          id: '0002',
          imgUrl:
            '//s.qunarzz.com/homenode/images/touchheader/train.png',
          desc: 'Train'
        },
        {
          id: '0003',
          imgUrl: '//s.qunarzz.com/homenode/images/touchheader/hotel.png',
          desc: 'Hotel'
        },
        {
          id: '0004',
          imgUrl:
            '//s.qunarzz.com/homenode/images/touchheader/train.png',
          desc: 'Train'
        },
        {
          id: '0005',
          imgUrl: '//s.qunarzz.com/homenode/images/touchheader/package.png',
          desc: 'Vacation'
        },
        {
          id: '0006',
          imgUrl: '//s.qunarzz.com/homenode/images/touchheader/piao.png',
          desc: 'tickets'
        },
        {
          id: '0007',
          imgUrl: '//s.qunarzz.com/homenode/images/touchheader/package.png',
          desc: 'Vacation'
        },
        {
          id: '0008',
          imgUrl: '//s.qunarzz.com/homenode/images/touchheader/package.png',
          desc: 'Vacation'
        },
        {
          id: '0009',
          imgUrl: '//s.qunarzz.com/homenode/images/touchheader/package.png',
          desc: 'Vacation'
        }
      ]
    }
  },
  computed: {
    pages () {
      const pages = []
      this.iconList.forEach((item, index) => {
        const page = Math.floor(index / 8)
        if (!pages[page]) {
          pages[page] = []
        }
        pages[page].push(item)
      })
      return pages
    }
  }
}
</script>

<style lang = "stylus" scoped>
@import '~styles/variables.styl';
@import '~styles/mixins.styl';

.icons >>> .swiper-container {
  height: 0;
  padding-bottom: 50%;

  .icon {
    position: relative;
    overflow: hidden;
    float: left;
    height: 0;
    width: 25%;
    padding-bottom: 25%;

    .icon-img {
      position: absolute;
      box-sizing: border-box;
      padding: 0.1rem;
      top: 0;
      right: 0;
      left: 0;
      bottom: 0.44rem;

      .icon-img-content {
        display: block;
        margin: 0 auto;
        height: 100%;
      }
    }

    .icon-desc {
      text-align: center;
      position: absolute;
      right: 0;
      left: 0;
      height: 0.44rem;
      line-height: 0.44rem;
      color: $darkTextColor;
      ellipsis()
    }
  }
}
</style>
