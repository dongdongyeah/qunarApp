<template>
  <div class='home'>
    <home-header></home-header>
    <home-swiper></home-swiper>
    <home-icon></home-icon>
    <home-like></home-like>
  </div>
</template>

<script>
import HomeHeader from './component/Header'
import HomeSwiper from './component/Swiper'
import HomeIcon from './component/Icon'
import HomeLike from './component/Like'
export default{
  name: 'Home',
  components: {
    HomeHeader,
    HomeSwiper,
    HomeIcon,
    HomeLike
  }
}
</script>

<style lang='stylus' scoped>
</style>
