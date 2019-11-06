<template>
  <div class='search-wrapper'>
    <input v-model='keyword' class='search' type='text' placeholder='请输入城市名或拼音'/>
    <ul class='search-list' v-show='hasInput'>
      <li
       v-for='item of keywordList'
        :key='item.id'
        class='border-bottom'
      >
        {{item.name}}
      </li>
      <li v-show='hasNotData'>没有找到匹配数据</li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'CitySearch',
  data () {
    return {
      keyword: '',
      keywordList: []
    }
  },
  props: {
    cities: Object
  },
  computed: {
    hasNotData () {
      return !this.keywordList.length
    },
    hasInput () {
      return this.keyword
    }
  },
  watch: {
    keyword () {
      const list = []
      for (let key in this.cities) {
        this.cities[key].forEach((value) => {
          if (value.name.indexOf(this.keyword) > -1 ||
          value.spell.indexOf(this.keyword) > -1) {
            list.push(value)
          }
        })
      }
      this.keywordList = list
    }
  }
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
      text-align: center
      padding: 0 4px 2px 4px
      font-size: 12px
      border-radius: 3px
    .search-list
      z-index: 3
      position: absolute
      top: 88px
      left: 0
      right: 0
      bottom: 0
      background: #eee
      li
        line-height: 30px
        text-indent: 5px
        background: #fff
</style>
