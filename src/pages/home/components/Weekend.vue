<template>
  <div class="weekend">
    <div class="weekend-title">周末去哪儿</div>
    <ul>
      <li class="item" v-for="item of list" :key="item.id">
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
  props: {
    list: Array
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
