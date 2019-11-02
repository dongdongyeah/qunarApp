<template>
  <div class='home'>
    <home-header></home-header>
    <home-swiper></home-swiper>
    <home-icon></home-icon>
    <home-like></home-like>
    <home-weekend></home-weekend>
  </div>
</template>

<script>
import HomeHeader from './component/Header'
import HomeSwiper from './component/Swiper'
import HomeIcon from './component/Icon'
import HomeLike from './component/Like'
import HomeWeekend from './component/Weekend'

export default{
  name: 'Home',
  components: {
    HomeHeader,
    HomeSwiper,
    HomeIcon,
    HomeLike,
    HomeWeekend
  }
}
</script>

<style lang='stylus' scoped>
</style>
