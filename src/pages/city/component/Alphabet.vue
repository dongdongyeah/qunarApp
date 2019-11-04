<template>
  <ul>
    <li v-for='(item, key) of cities' :key='key'>{{key}}</li>
  </ul>
</template>

<script>
export default {
  name: 'CityAlphabet',
  props: {
    cities: Object
  }
}
</script>

<style lang='stylus' scoped>
@import '~styles/varivles.styl'
  ul
    position: absolute
    z-index: 99
    top: 85px
    right: 0
    bottom: 0
    width: 20px
    text-align: center
    display: flex
    flex-direction: column
    justify-content: center
    li
      margin-top: 2px
      color: $bgColor
</style>
