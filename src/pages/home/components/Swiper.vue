<template>
  <div class="wrapper">
    <swiper :options="swiperOption">
          <!-- slides -->
          <swiper-slide v-for="item of swiperList" :key="item.id">
            <img class="swiper-img" :src="item.imgUrl"/>
          </swiper-slide>
          <!-- Optional controls -->
          <div class="swiper-pagination"  slot="pagination"></div>
        </swiper>
  </div>

</template>

<script>
export default {
  name: 'HomeSwiper',
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true
      },
      swiperList: [{
        id: '0001',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1801/bd/04554e7c67650302.jpg_640x200_cd2a40cb.jpg'
      },
      {
        id: '0002',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/5c/969bfa7af00a2702.jpg_640x200_e1b76963.jpg'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
.wrapper >>> .swiper-pagination-bullet-active
    background: #fff
.wrapper
  overflow: hidden
  width: 100%
  height: 0
  padding-bottom: 31.25%
  background: #eee
  .swiper-img
    width: 100%
</style>
