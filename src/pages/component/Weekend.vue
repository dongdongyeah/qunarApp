<template>
  <div class='weekend'>
    <div class='header'>周末去哪儿</div>
    <div v-for='item of list' :key='item.id'>
      <img class='img' :src='item.imgUrl'/>
      <div class='text'>
        <p class='title'>{{item.title}}</p>
        <p class='desc'>{{item.desc}}</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HomeWeekend',
  props: {
    list: Array
  }
}
</script>

<style lang='stylus' scoped>
  .header
    height: 50px
    line-height: 50px
    font-size: 16px
    background: rgb(245,245,245)
    text-indent: 15px
  .img
    width: 100%
  .text
    padding: 10px
    .title
      font-size: 16px
      margin-bottom: 10px
    .desc
      font-size: 14px
</style>
