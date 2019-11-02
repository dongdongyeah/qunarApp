<template>
  <div class='home'>
    <home-header></home-header>
    <home-swiper></home-swiper>
    <home-icon></home-icon>
  </div>
</template>

<script>
import HomeHeader from './component/Header'
import HomeSwiper from './component/Swiper'
import HomeIcon from './component/Icon'
export default{
  name: 'Home',
  components: {
    HomeHeader,
    HomeSwiper,
    HomeIcon
  }
}
</script>

<style lang='stylus' scoped>

</style>
