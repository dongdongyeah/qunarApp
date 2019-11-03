<template>
  <div class='header'>
    <div class='back'>
      <span class='iconfont icon-back'>&#xe6db;</span>
    </div>
    <div class='search'>
      <span class='iconfont icon-search'>&#xe6e1;</span>
      <p class='search-p'>输入城市/景点/游玩主题</p>
    </div>
    <div class='city'>
      {{this.city}}
      <span class='iconfont icon-city'>&#xe64a;</span>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HomeHeader',
  props: {
    city: String
  }
}
</script>

<style lang='stylus' scoped>
@import '~styles/varivles.styl'
  .header
    display: flex
    height: 44px
    line-height: 44px
    font: 14px
    background: $bgColor
    color: #fff
    .back
      width: 40px
      text-align: center
      .icon-back
        font-size: 28px
    .search
      position: relative
      top: 7px
      flex: 1
      height: 30px
      line-height: 30px
      border-radius: 3px
      background: #fff
      color: #e4e7ea
      .icon-search
        position: absolute
        font-size:20px
        left: 5px
        top: 2px
      .search-p
        position: absolute
        top: 0
        left: 25px
    .city
      width: 64px
      text-align: center
      .icon-city
        font-size: 10px
</style>
