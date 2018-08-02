<template>
  <div class="">
    <div class="recommend-title"><img class="heart" src="http://img1.qunarzz.com/piao/fusion/1711/89/ebc329f16c55bb02.png" alt="">猜你喜欢</div>
    <ul>
      <li class="item" v-for="item of recommend" :key="item.id">
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
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeRecommend',
  data () {
    return {
      recommend: [{
        id: '0001',
        title: '北京国际鲜花港',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1803/12/126471e0966aca5ba3.img.jpg_200x200_f1286016.jpg',
        comment: 1930,
        price: 19.9,
        location: '顺义区'
      }, {
        id: '0002',
        title: '北京欢乐谷',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1508/a5/4003f9dd7bebf61eccbf64046e26d487.water.jpg_200x200_7690e4cd.jpg',
        comment: 55871,
        price: 62,
        location: '朝阳区'
      }, {
        id: '0003',
        title: '故宫',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1409/19/adca619faaab0898245dc4ec482b5722.jpg_200x200_1bc99086.jpg',
        comment: 252407,
        price: 20,
        location: '东城区'
      }, {
        id: '0004',
        title: '北京欢乐水魔方',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/201405/23/0265195fc4b7913a758674357c3cc8f6.jpg_200x200_b58ea00b.jpg',
        comment: 2941,
        price: 111,
        location: '丰台区'
      }, {
        id: '0005',
        title: '水乐方嬉水乐园',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1501/c2/c212a154649088c1.water.jpg_200x200_69d1df69.jpg',
        comment: 1630,
        price: 228.5,
        location: '水立方'
      }, {
        id: '0006',
        title: '古北水镇',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1804/c8/c88bb5e69c9a9c5ea3.img.jpg_200x200_740720ff.jpg',
        comment: 7070,
        price: 150,
        location: '密云县'
      }, {
        id: '0007',
        title: '北京野生动物园',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1507/36/ce3d2d6c9ab44d67ae68d940b8781829.water.jpg_200x200_0938a8f2.jpg',
        comment: 11834,
        price: 71,
        location: '大兴区'
      }, {
        id: '0008',
        title: '北京杜莎夫人蜡像馆',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1608/4f/4fc3f5a1b838f279a3.water.jpg_200x200_e6528ef6.jpg',
        comment: 6473,
        price: 85,
        location: '前门大街'
      }]
    }
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
