<template>
  <div class='swiper'>
    <swiper :options="swiperOption">
      <!-- slides -->
      <swiper-slide v-for="item of this.list" :key="item.id">
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
      }
    }
  },
  props: {
    list: Array
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
