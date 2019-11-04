<template>
  <div class='search-wrapper'>
    <input class='search' type='text' placeholder='请输入城市名或拼音'/>
  </div>
</template>

<script>
export default {
  name: 'CitySearch'
}
</script>

<style lang='stylus' scoped>
@import '~styles/varivles.styl'
  .search-wrapper
    height: 40px
    line-height: 40px
    padding: 2px 5px 2px 5px
    background: $bgColor
    .search
      box-sizing: border-box
      width: 100%
      height: 25px
      padding: 0 4px 2px 4px
      font-size: 13px
      border-radius: 3px
</style>
