<template>
  <div class="wrapper">
    <swiper :options="swiperOption">
      <swiper-slide v-for="item of swiperList" :key="item.id">
        <img class="swiper-img" :src="item.imgUrl" alt="" />
      </swiper-slide>
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
      swiperList: [
        {
          id: '0001',
          imgUrl: 'http://img1.qunarzz.com/piao/fusion/1809/d4/e298dff35d3af802.jpg_750x200_9b0d56c1.jpg'
        },
        {
          id: '0002',
          imgUrl: 'http://img1.qunarzz.com/piao/fusion/1801/6f/3bf4c3ba2864d602.jpg_750x200_2881def8.jpg'
        }
      ]
    }
  }
}
</script>
<style lang='stylus' scoped>
.wrapper >>> .swiper-pagination-bullet-active {
  background: #fff;
}

.wrapper {
  width: 100%;
  height: 0;
  overflow: hidden;
  padding-bottom: 26.67%;
  background: #eee;

  .swiper-img {
    width: 100%;
  }
}
</style>
