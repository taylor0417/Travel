<template>
  <div class="">
    <div class="search">
      <input v-model="keyword" class="searchInput" type="text" name="" value="" placeholder="输入城市名或拼音">
    </div>
    <div
        class="search-content"
        ref="search"
        v-show="keyword"
    >
      <ul>
        <li class="search-item border-bottom"
            v-for="item of list"
            :key="item.id"
            @click="handleCityClick(item.name)"
        >{{item.name}}</li>
        <li class="search-item border-bottom" v-show="hasNoData">没有找到匹配数据</li>
      </ul>
    </div>
  </div>
</template>

<script>
import Bscroll from 'better-scroll'
export default {
  name: 'CitySearch',
  props: {
    cities: Object
  },
  data () {
    return {
      keyword: '',
      list: [],
      timer: null
    }
  },
  computed: {
    hasNoData () {
      return !this.list.length
    }
  },
  watch: {
    keyword () {
      if (this.timer) {
        clearTimeout(this.timer)
      }
      if (!this.keyword) {
        this.list = []
        return
      }
      this.timer = setTimeout(() => {
        const result = []
        for (let i in this.cities) {
          this.cities[i].forEach((value) => {
            if (value.spell.indexOf(this.keyword) > -1 || value.name.indexOf(this.keyword) > -1) {
              result.push(value)
            }
          })
        }
        this.list = result
      }, 100)
    }
  },
  methods: {
    handleCityClick (city) {
      this.$store.commit('changeCity', city)
      this.$router.push('/')
    }
  },
  mounted () {
    this.scroll = new Bscroll(this.$refs.search)
  }
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
  .search-content
    position: absolute
    top: 1.4rem
    left: 0
    right: 0
    bottom: 0
    overflow: hidden
    background: #eee
    z-index: 1
    .search-item
      line-height: .62rem
      padding-left: .2rem
      background: #fff
      color: #666
</style>
