<template>
  <div class='like'>
    <div class='like-top'>
      <p class='title'><span class='iconfont iconfont-like'>&#xe757;</span>猜你喜欢</p>
    </div>
    <div class='like-list border-bottom' v-for='item of list' :key='item.id'>
      <img class='like-img' :src='item.imgUrl'/>
      <div class='like-info'>
        <p class='info-title'>{{item.title}}</p>
        <div class='info-start'>
          <span class='iconfont iconfont-star'>&#xe6a3;&#xe6a3;&#xe6a3;&#xe6a3;&#xe6a3;</span>
          <span>{{item.comment}}</span><span>条评论</span>
        </div>
        <div class='info-center'>
          <span class='start'>￥</span>
          <span class='center'>{{item.price}}</span>
          <span class='end'>起</span>
          <span class='address'>{{item.place}}</span>
        </div>
        <p class='info-end'>{{item.desc}}</p>
      </div>
  </div>
  </div>
</template>

<script>
export default {
  name: 'HomeLike',
  props: {
    list: Array
  }
}
</script>

<style lang='stylus' scoped>
  .like-top
    margin-top: 5px
    height: 50px
    background: rgb(245,245,245)
    .title
      height: 20px
      padding: 15px
      font-size: 16px
      .iconfont-like
        color: rgb(255,90,89)
        margin-right: 5px
  .like-list
    display: flex
    padding-bottom: 15px
    .like-img
      width: 100px
      height: 100px
      margin: 10px
    .like-info
      color: #212121
      padding: 10px
      .info-title
        font-size: 16px
        margin-bottom: 10px
      .info-start
        margin-bottom: 10px
        .iconfont-star
          color: #ffb436
          font-size: 13px
          margin-right: 8px
      .info-center
        color: #ff8300
        margin-bottom: 25px
        .start
          font-size: 12px
        .center
          font-size: 20px
        .end
          color: #212121
        .address
          position: absolute
          color: #212121
          right: 15px
          font-size: 12px
      .info-end
        color: #ff5555
</style>
