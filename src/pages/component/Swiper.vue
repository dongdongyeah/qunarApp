<template>
  <div class='swiper'>
    <swiper :options="swiperOption">
      <!-- slides -->
      <swiper-slide v-for="item of swiperList" :key="item.id">
        <img class='swiper-img' :src="item.imgUrl"/>
      </swiper-slide>
      <!-- Optional controls -->
      <div class="swiper-pagination" slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeSwiper',
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true,
        autoplay: 5000,
        autoplayDisableOnInteraction: false /* 使用swiper后仍然autoplay */
      },
      swiperList: [{
        id: '0001',
        imgUrl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/201910/c8762210baff5ade1a3b2fe0ab914992.png_750x200_9bbb2f51.png'
      }, {
        id: '0002',
        imgUrl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/201910/fcc952d6b479db0e7e61922f3ee70f04.jpg_750x200_c5b67f70.jpg'
      }]
    }
  }
}
</script>

<style lang='stylus' scoped>
    .swiper >>> .swiper-pagination-bullet-active
      background: #fff !important
    .swiper
      overflow: hidden
      height: 0
      padding-bottom: 26.7%
      background: #ccc
    .swiper-img
      width: 100%
</style>
