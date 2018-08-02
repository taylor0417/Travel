<template>
  <div class="weekend">
    <div class="weekend-title">周末去哪儿</div>
    <ul>
      <li class="item" v-for="item of weekendList" :key="item.id">
        <div class="img-wrapper">
          <img class="item-img" :src="item.imgUrl" alt="">
        </div>
        <div class="itme-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeWeekend',
  data () {
    return {
      weekendList: [{
        id: '0001',
        title: '漂流勇进，烧烤露营',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1606/85/c6b6bad1b977e.jpg_r_640x214_5c638941.jpg',
        desc: '轻松水上漂，任我乐逍遥'
      }, {
        id: '0001',
        title: '北京清凉避暑胜地',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1505/53/02091f1ee43d0a.jpg_r_640x214_2e3256b1.jpg',
        desc: '到大自然中享受“天然空调”的清凉'
      }, {
        id: '0001',
        title: '北京必游TOP10',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1505/aa/7baaf8a851d221.jpg_r_640x214_1431200f.jpg',
        desc: '来北京必去的景点非这些地方莫属'
      }, {
        id: '0001',
        title: '寻找北京的皇城范儿',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1505/9e/21df651e19af5d.jpg_r_640x214_3ea5bb38.jpg',
        desc: '数百年的宫廷庙宇，至今依旧威严霸气'
      }, {
        id: '0001',
        title: '学生最爱的博物馆',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1505/ce/bc89bc2f0e33ea.jpg_r_640x214_3e408453.jpg',
        desc: '周末干嘛？北京很多博物馆已经免费开放啦'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import '~style/mixin.styl'
  .weekend-title
    line-height: .8rem
    text-indent: .2rem
  .item
    overflow: hidden
    background: #FFF
    .img-wrapper
      padding-bottom: 38%
      height: 0
      .item-img
        width: 100%
    .itme-info
      padding: .14rem .2rem .2rem .2rem
      .item-title
        font-size: .28rem
        line-height: .48rem
        padding-right: 1.4rem
        ellipsis()
      .item-desc
        font-size: .24rem
        line-height: .42rem
        color: #616161
        padding-right: 1.4rem
        ellipsis()
</style>
