<template>
  <div>
    <div class="title">周末去哪儿</div>
    <ul>
      <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
        <img class="item-img" :src='item.imgUrl'/>
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
          <button class="item-button">查看详情</button>
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
      recommendList: [{
        id: '0001',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/201408/14/771e7f0a85ca13b12c3fde0f7739440f.jpg_200x200_5e08c104.jpg',
        title: '杭州海洋世界',
        desc: '领略海洋的美,领略海洋的美,领略海洋的美,领略海洋的美,领略海洋的美'
      },
      {
        id: '0002',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/201408/14/771e7f0a85ca13b12c3fde0f7739440f.jpg_200x200_5e08c104.jpg',
        title: '杭州海洋世界',
        desc: '领略海洋的美,领略海洋的美,领略海洋的美,领略海洋的美,领略海洋的美'
      },
      {
        id: '0003',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/201408/14/771e7f0a85ca13b12c3fde0f7739440f.jpg_200x200_5e08c104.jpg',
        title: '杭州海洋世界',
        desc: '领略海洋的美,领略海洋的美,领略海洋的美,领略海洋的美,领略海洋的美'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/mixins.styl'
  .title
    margin-top: .2rem
    line-height: .8rem
    background: #eee
    text-indent: .2rem
  .item
    overflow: hidden
    display: flex
    height: 1.9rem
    .item-img
      width: 1.7rem
      height: 1.7rem
      padding: .1rem
    .item-info
      flex: 1
      padding: .1rem
      min-width: 0
      .item-title
        line-height: .54rem
        font-size: .32rem
        ellipsis()
      .item-desc
        line-height: .4rem
        color: #ccc
        ellipsis()
      .item-button
        line-height: .44rem
        margin-top: .2rem
        background: #ff9300
        padding: 0 .2rem
        border-radius: .06rem
        color: #fff
</style>
