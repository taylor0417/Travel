<template>
    <ul class="list">
      <li class="item" v-for="(item, key) of cities" :key="key">{{key}}</li>
    </ul>
</template>

<script>
export default {
  name: 'CityAlphabet',
  props: {
    cities: Object
  }
}
</script>

<style lang="stylus" scoped="">
  @import '~style/varibles.styl'
  .list
    display: flex
    flex-direction: column
    justify-content: center
    position: absolute
    right: .1rem
    top: 1.58rem
    bottom: 0
    width: .4rem
    .item
      text-align: center
      line-height: .4rem
      color: $bgColor
</style>
