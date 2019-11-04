<template>
  <ul>
    <li>A</li>
    <li>A</li>
    <li>A</li>
    <li>A</li>
    <li>A</li>
    <li>A</li>
    <li>A</li>
    <li>A</li>
  </ul>
</template>

<script>
export default {
  name: 'CityAlphabet'
}
</script>

<style lang='stylus' scoped>
@import '~styles/varivles.styl'
  ul
    position: absolute
    z-index: 99
    top: 85px
    right: 5px
    bottom: 0
    display: flex
    flex-direction: column
    justify-content: center
    li
      margin-top: 2px
      color: $bgColor
</style>
