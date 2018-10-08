<template>
  <div>
      <div class="recommend-title">周末去哪儿</div>
      <ul>
        <li
          class="item border-bottom"
          v-for="item of recommendList"
          :key="item.id"
        >
          <div class="item-img-wrapper">
            <img class="item-img" :src="item.imgUrl" alt="" />
          </div>
          <div class="item-info">
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
  data () {
    return {
      recommendList: [{
        id: '0001',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1509/a1/4faeed396a85aa.jpg_r_640x214_75530e9b.jpg',
        title: '北京野生动物园',
        desc: '北京野生动物园激情人生'
      }, {
        id: '0002',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1509/a1/4faeed396a85aa.jpg_r_640x214_75530e9b.jpg',
        title: '北京野生动物园',
        desc: '北京野生动物园激情人生'
      }, {
        id: '0003',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1509/a1/4faeed396a85aa.jpg_r_640x214_75530e9b.jpg',
        title: '北京野生动物园',
        desc: '北京野生动物园激情人生'
      }]
    }
  }
}
</script>
<style lang='stylus' scoped>
@import '~styles/mixins.styl'
  .recommend-title
    line-height .8rem
    text-indent .2rem
    margin-top .2rem
    background #eee
  .item-img-wrapper
    overflow hidden
    height 0
    padding-bottom 33.9%
    .item-img
      width 100%
  .item-info
    padding .1rem
    .item-title
      line-height .54rem
      font-size .32rem
      ellipsis()
    .item-desc
      line-height .4rem
      color #ccc
      ellipsis()
</style>
