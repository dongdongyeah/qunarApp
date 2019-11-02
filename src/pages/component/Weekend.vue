<template>
  <div class='weekend'>
    <div class='header'>周末去哪儿</div>
    <div v-for='item of weekendList' :key='item.id'>
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
  data () {
    return {
      weekendList: [{
        id: '0001',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1811/f3/86173f863bef61.jpg_r_640x214_52b003ac.jpg',
        title: '京城周末撒欢',
        desc: '在帝都过周末，不仅仅是城中游！'
      }, {
        id: '0002',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1811/f3/86173f863bef61.jpg_r_640x214_52b003ac.jpg',
        title: '京城周末撒欢',
        desc: '在帝都过周末，不仅仅是城中游！'
      }, {
        id: '0003',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1811/f3/86173f863bef61.jpg_r_640x214_52b003ac.jpg',
        title: '京城周末撒欢',
        desc: '在帝都过周末，不仅仅是城中游！'
      }]
    }
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
