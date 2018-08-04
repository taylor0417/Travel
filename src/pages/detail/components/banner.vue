<template>
  <div class="banner" @click="handleBannerClick">
    <img class="banner-img" src="//img1.qunarzz.com/sight/p0/1803/12/126471e0966aca5ba3.img.jpg_600x330_8b04e389.jpg" alt="">
    <span class="iconfont banner-back" @click.stop="handleBannerBack">&#xe624;</span>
    <div class="banner-info">
      <div class="banner-number">
        <span class="iconfont header-number-icon">&#xe6dd;</span>38
      </div>
      <div class="banner-title">
        北京国际鲜花港(AAAA景区)
      </div>
    </div>
    <common-gallary :imgs="imgs" v-show="showGallary" @close="handleGallaryClose"></common-gallary>
  </div>
</template>

<script>
import CommonGallary from 'common/gallary/Gallary'
export default {
  name: 'DetailBanner',
  data () {
    return {
      imgs: ['http://img1.qunarzz.com/sight/p0/1803/12/126471e0966aca5ba3.img.jpg_r_800x800_fd14650b.jpg', 'http://img1.qunarzz.com/sight/p0/1806/5b/5b32a9e1ac462fb5a3.img.jpg_r_800x800_ba8d7dcd.jpg', 'http://img1.qunarzz.com/sight/p0/1806/42/424741acd6ec0563a3.img.jpg_r_800x800_e7b4a7b4.jpg'],
      showGallary: false
    }
  },
  methods: {
    handleBannerClick () {
      this.showGallary = true
    },
    handleGallaryClose () {
      this.showGallary = false
    },
    handleBannerBack () {
      this.showGallary = false
      this.$router.push('/')
    }
  },
  components: {
    CommonGallary
  }
}
</script>

<style lang="stylus" scoped>
  .banner
    position: relative
    overflow: hidden
    height: 0
    width: 100%
    padding-bottom: 55%
    .banner-img
      width: 100%
    .banner-info
      display: flex
      position: absolute
      left: 0
      right: 0
      bottom: 0
      line-height: .6rem
      .banner-title
        position: absolute
        right: .2rem
        bottom: .36rem
        left: .2rem
        font-size: .36rem
        line-height: .4rem
        color: #fff
        z-index: 1
        text-shadow: 0 1px 2px rgba(0,0,0,0.7)
      .banner-number
        position: absolute
        left: .2rem
        bottom: .86rem
        width: 1.2rem
        background: rgba(0,0,0,.5)
        border-radius: .2rem
        font-size: .24rem
        color: #fff
        line-height: .4rem
        text-align: center
        .header-number-icon
          position: relative;
          top: .02rem;
          font-size: .24rem;
          color: #fff;
          margin-right: .1rem
    .banner-back
      position: absolute
      left: .1rem
      top: .1rem
      display: block
      line-height: .72rem
      text-align: center
      color: #fff
      display: block
      font-size: .36rem
      width: .72rem
      height: .72rem
      background-color: rgba(0,0,0,0.5)
      border-radius: .36rem

</style>
