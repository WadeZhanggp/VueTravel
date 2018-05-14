<template>
  <!--<div class="wrapper">-->
    <!--<swiper :options="swiperOption">-->
          <!--&lt;!&ndash; slides &ndash;&gt;-->
          <!--<swiper-slide v-for="item of swiperList" :key="item.id">-->
            <!--<img class="swiper-img" :src="item.imgUrl"/>-->
          <!--</swiper-slide>-->
          <!--&lt;!&ndash; Optional controls &ndash;&gt;-->
          <!--<div class="swiper-pagination"  slot="pagination"></div>-->
    <!--</swiper>-->
  <!--</div>-->
  <div class="">
    <el-carousel indicator-position="outside">
      <el-carousel-item v-for="item in 4" :key="item">
        <h3>{{ item }}</h3>
      </el-carousel-item>
    </el-carousel>
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
  .el-carousel__item h3 {
    color: #475669;
    font-size: 18px;
    opacity: 0.75;
    line-height: 300px;
    margin: 0;
  }

  .el-carousel__item:nth-child(2n) {
    background-color: #99a9bf;
  }

  .el-carousel__item:nth-child(2n+1) {
    background-color: #d3dce6;
  }
</style>
