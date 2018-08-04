<template>
  <div class="">
    <div class="recommend-title"><img class="heart" src="http://img1.qunarzz.com/piao/fusion/1711/89/ebc329f16c55bb02.png" alt="">猜你喜欢</div>
    <ul>
      <router-link
          tag="li"
          class="item"
          v-for="item of list"
          :key="item.id"
          :to="'/detail/' + item.id"
      >
        <div class="img-wrapper">
          <span class="tips">购买随用</span>
          <img class="item-img" :src="item.imgUrl" alt="">
        </div>
        <div class="itme-info">
          <p class="item-title">{{item.title}}</p>
          <div class="item-desc">
            <div class="stars">
              <span class="iconfont stars-icon">&#xe676;</span>
              <span class="iconfont stars-icon">&#xe676;</span>
              <span class="iconfont stars-icon">&#xe676;</span>
              <span class="iconfont stars-icon">&#xe676;</span>
              <span class="iconfont stars-icon">&#xe676;</span>
            </div>
            <p class="comment">
              <span>{{item.comment}}</span>条评论
            </p>
          </div>
          <p class="item-price">
            ￥<span class="price">{{item.price}}</span>起
            <span class="location">{{item.location}}</span>
          </p>
        </div>
      </router-link>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeRecommend',
  props: {
    list: Array
  }
}
</script>

<style lang="stylus" scoped>
  @import '~style/mixin.styl'
  .recommend-title
    margin-top: .2rem
    line-height: .8rem
    background: #fff
    text-indent: .2rem
    .heart
      width: .3rem
      height: .3rem
      margin-right: .08rem
  .item
    display: flex
    height: 2rem
    overflow: hidden
    padding: .2rem
    border-bottom: 1px solid #e0e0e0
    background: #FFF
    .img-wrapper
      width: 2rem
      height: 2rem
      position: relative
      .item-img
        width: 2rem
        height: 2rem
      .tips
        position: absolute
        display: block
        height: .38rem
        line-height: .38rem
        text-indent: .04rem
        width: 1.02rem
        font-size: .2rem
        color: #fff
        background: url(https://img1.qunarzz.com/piao/fusion/1802/20/2ba6d10b17972e02.png) center center no-repeat
        background-size: 1.02rem .38rem
    .itme-info
      padding-left: .22rem
      width: 100%
      .item-title
        margin-top: .26rem
        height: .44rem
        color: #212121
        font-size: .32rem
        line-height: .44rem
        ellipsis()
      .item-desc
        margin-top: .14rem
        height: .34rem
        line-height: .34rem
        .stars
          float: left
          width: 1.7rem
          height: .28rem
          line-height: .28rem
          .stars-icon
            display: inline-block
            color: #ffb436
            font-size: .24rem
        .comment
          font-size: .24rem
      .item-price
        margin-top: .22rem
        font-size: .24rem
        .price
          font-size: .4rem
          color: #ff8300
        .location
          float: right
          margin-top: .15rem
          margin-right: .24rem
</style>
