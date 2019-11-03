<template>
  <div class='header'>
    城市选择
    <router-link to='/'>
      <div class='iconfont back'>&#xe6db;</div>
    </router-link>
  </div>
</template>

<script>
export default {
  name: 'CityHeader'
}
</script>

<style lang='stylus' scoped>
@import '~styles/varivles.styl'
  .header
    height: 44px
    line-height: 44px
    text-align: center
    font-size: 18px
    color: #fff
    background: $bgColor
    .back
      position: absolute
      top: 0
      left: 5px
      font-size: 28px
      color: #fff
</style>
