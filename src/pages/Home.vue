<template>
  <div class='home'>
    <home-header></home-header>
    <home-swiper></home-swiper>
    <div>test</div>
  </div>
</template>

<script>
import HomeHeader from './component/Header'
import HomeSwiper from './component/Swiper'
export default{
  name: 'Home',
  components: {
    HomeHeader,
    HomeSwiper
  }
}
</script>

<style lang='stylus' scoped>

</style>
