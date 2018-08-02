<template>
  <div class="search">
    <input class="searchInput" type="text" name="" value="" placeholder="输入城市名或拼音">
  </div>
</template>

<script>
export default {
  name: 'CitySearch'
}
</script>

<style lang="stylus" scoped="">
  @import '~style/varibles.styl'
  .search
    height: .72rem
    background: $bgColor
    padding: .1rem .1rem
    box-sizing: border-box
    .searchInput
      box-sizing: border-box
      padding: 0 0.1rem
      height: .5rem
      line-height: .5rem
      text-align: center
      border-radius: .06rem
      width: 100%
      color: #666
</style>
