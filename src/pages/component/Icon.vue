<template>
  <swiper :options="swiperOption">
    <swiper-slide class='icons' v-for='page of pages' :key='page.index'>
      <li class='icon' v-for='item of page' :key='item.id'>
        <div class='icon-wrap'>
          <img class='icon-img' :src='item.imgUrl'/>
        </div>
        <p class='icon-title'>{{item.title}}</p>
      </li>
    </swiper-slide>
    <div class="swiper-pagination" slot="pagination"></div>
  </swiper>
</template>

<script>
export default {
  name: 'HomeIcon',
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        autoplay: false
      },
      iconList: [{
        id: '0001',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
        title: '景点门票'
      }, {
        id: '0002',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
        title: '景点门票'
      }, {
        id: '0003',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
        title: '景点门票'
      }, {
        id: '0004',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
        title: '景点门票'
      }, {
        id: '0005',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
        title: '景点门票'
      }, {
        id: '0006',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
        title: '景点门票'
      }, {
        id: '0007',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
        title: '景点门票'
      }, {
        id: '0008',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
        title: '景点门票'
      }, {
        id: '0009',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
        title: '景点门票'
      }, {
        id: '0010',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
        title: '景点门票'
      }]
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

<style lang='stylus' scoped>
  .icons
    overflow: hidden
    height: 0
    padding-bottom: 50%
    .icon
      position: relative
      float: left
      width: 25%
      height: 0
      padding-bottom: 25%
      .icon-wrap
        position: absolute
        top: 0
        left: 0
        right: 0
        bottom: 20px
        padding-top: 5px
        text-align: center
        background: #fff
        .icon-img
          height: 100%
      .icon-title
        position: absolute
        text-align: center
        line-height: 20px
        left: 0
        right: 0
        bottom: 0
</style>
