<template>
  <div class='city-list' ref='wrapper'>
    <div class='wrapper'>
      <div class='area'>
        <div class='title border-topbottom'>您的位置</div>
        <div class='list'>
          <div class='city-wrapper your-position'>
            <div class='city your-position'>北京</div>
          </div>
        </div>
      </div>
      <div class='area'>
        <div class='title border-topbottom'>热门城市</div>
        <div class='list'>
          <div class='city-wrapper' v-for='item of hotCities' :key='item.id'>
            <div class='city'>{{item.name}}</div>
          </div>
        </div>
      </div>
      <div class='area'
       v-for='(item, key) of cities'
        :key='key'
        :ref='key'
      >
        <div class='title border-topbottom'>{{key}}</div>
        <ul>
          <li class='city-li  border-topbottom' v-for='innerItem of item' :key='innerItem.id'>{{innerItem.name}}</li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
import BScroll from 'better-scroll'
export default {
  name: 'CityList',
  props: {
    hotCities: Array,
    cities: Object,
    letter: String
  },
  watch: {
    letter () {
      if (this.letter) {
        const element = this.$refs[this.letter][0]
        this.scroll.scrollToElement(element)
      }
    }
  },
  mounted () {
    this.scroll = new BScroll(this.$refs.wrapper)
  }
}
</script>

<style lang='stylus' scoped>
@import '~styles/varivles.styl'
  .city-list
    position: absolute
    top: 88px
    left: 0
    right: 0
    bottom:0
    overflow: hidden
    .title
      height: 25px
      line-height: 25px
      background: #eee
      text-indent: 10px
    .list
      display: flow-root
      padding: 10px 15px
      .city-wrapper
        float: left
        width: 75px
        height: 15px
        line-height: 15px
        text-align: center
        border: 1px solid #ccc
        border-radius: 3px
        padding: 5px 10px
        margin: 5px
      .your-position
        color: $bgColor
        border-color: $bgColor
    .city-li
      line-height: 30px
      text-indent: 10px
</style>
