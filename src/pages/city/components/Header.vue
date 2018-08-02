<template>
  <div class="header">
    城市选择
    <router-link to="/">
      <div class="iconfont header-back">&#xe624;</div>
    </router-link>
  </div>
</template>

<script>
export default {
  name: 'CityHeader'
}
</script>

<style lang="stylus" scoped="">
  @import '~style/varibles.styl'
  .header
    position: relative
    overflow: hidden
    height: .68rem
    line-height: .68rem
    color: #fff
    text-align: center
    background: $bgColor
    font-size: .32rem
    .header-back
      position: absolute
      top: 0
      left: 0
      width: .8rem
      height: .88rem
      line-height: .88rem
      font-size: .36rem
      color: #fff
</style>
