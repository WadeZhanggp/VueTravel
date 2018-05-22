<template>
  <div>
    <div class="banner" @click="handleBannerClick">
      <img class="banner-img" src="http://img1.qunarzz.com/sight/p0/1412/be/c788f0f3767d2ea037b9b66d2010bfa4.water.jpg_600x330_86333333.jpg">
      <div class="banner-info">
        <div class="banner-title">宋城千古情</div>
        <div class="banner-number"><span class="iconfont banner-icon">&#xe692;</span>22</div>
      </div>
    </div>
    <common-gallary
      :imgs="imgs"
      v-show="showGallary"
      @close="handleGallaryClose"
    ></common-gallary>
  </div>
</template>

<script>
import CommonGallary from '../../common/gallary/Gallary'
export default {
  name: 'DetailBanner',
  data () {
    return {
      showGallary: false,
      imgs: ['http://img1.qunarzz.com/sight/p0/1412/be/c788f0f3767d2ea037b9b66d2010bfa4.water.jpg_600x330_86333333.jpg', 'http://img1.qunarzz.com/sight/p0/1412/be/c788f0f3767d2ea037b9b66d2010bfa4.water.jpg_600x330_86333333.jpg', 'http://img1.qunarzz.com/sight/p0/1412/be/c788f0f3767d2ea037b9b66d2010bfa4.water.jpg_600x330_86333333.jpg']
    }
  },
  methods: {
    handleBannerClick () {
      this.showGallary = true
    },
    handleGallaryClose () {
      this.showGallary = false
    }
  },
  components: {CommonGallary},
  comments: {
    CommonGallary
  }
}
</script>

<style lang="stylus" scoped>
.banner
  position relative
  overflow hidden
  padding-bottom 55%
  height 0
  .banner-img
    width 100%
  .banner-info
    display flex
    position absolute
    left 0
    right 0
    color #fff
    line-height .6rem
    background-image linear-gradient(top, rgba(0, 0, 0, 0), rgba(0, 0, 0, 0.8))
    bottom 0
    .banner-title
      flex 1
      font-size .32rem
      padding 0 .2rem
    .banner-number
      margin-top .14rem
      padding 0 .4rem
      height .32rem
      line-height .32rem
      background rgb(0, 0, 0, .8)
      font-size .24rem
      border-radius .2rem
      .banner-icon
        font-size .24rem
</style>
