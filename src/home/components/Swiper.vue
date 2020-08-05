<template>
  <swiper :options="swiperOptions">
    <swiper-slide v-for="item of swiperList" :key="item.id">
      <img class="swiper-img" :src="item.src" alt="test" />
    </swiper-slide>
    <div class="swiper-pagination" slot="pagination"></div>
  </swiper>
</template>

<script>
export default {
  name: 'HomeSwiper',

  data () {
    return {
      swiperOptions: {
        loop: true
      },
      swiperList: [{
        id: 1,
        src: 'https://imgs.qunarzz.com/vs_ceph_vcimg/b8c4527c41649814cc4cf86880abba54.jpeg'
      }, {
        id: 2,
        src: 'https://imgs.qunarzz.com/vc/e3/a1/71/f498dfd3bed948d623c9093252.jpg_92.jpg'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  .swiper-img
    width: 100%
</style>
