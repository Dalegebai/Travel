<template>
  <div class="icons">
    <swiper>
      <swiper-slide v-for="(page,index) of pages" :key="index">
        <div class="icon" v-for="item of page" :key="item.id">
          <div class="icon-img">
            <img class="icon-img-content" :src="item.imgSrc" :alt="item.desc"/>
          </div>
          <p class="icon-desc">{{item.desc}}</p>
        </div>
      </swiper-slide>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeIcons',
  data () {
    return {
      iconList: [{
        id: 1,
        imgSrc: 'https://picbed.qunarzz.com/01d2f57f920666364197a850dab859a8.png',
        desc: '民俗客栈'
      }, {
        id: 2,
        imgSrc: 'https://picbed.qunarzz.com/83af731055e121a3251690b225327b56.png',
        desc: '专车自驾'
      }, {
        id: 3,
        imgSrc: 'https://picbed.qunarzz.com/5b6737be49ca243072ca614f07803b83.png',
        desc: '赚钱·信用卡'
      }, {
        id: 4,
        imgSrc: 'https://picbed.qunarzz.com/1e107321f5396ea4994cd832232ecf8a.png',
        desc: '旅游团购'
      }, {
        id: 5,
        imgSrc: 'https://picbed.qunarzz.com/c65b3bb7571a6bd62df669213e44b84d.png',
        desc: '一日游'
      }, {
        id: 6,
        imgSrc: 'https://picbed.qunarzz.com/f6bb08a239ce1b038204120a8d1e4669.png',
        desc: '特惠酒店'
      }, {
        id: 7,
        imgSrc: 'https://picbed.qunarzz.com/3a08f360e958ccb2b947049387873ace.png',
        desc: '借钱'
      }, {
        id: 8,
        imgSrc: 'https://picbed.qunarzz.com/19b4f6d2fabd617789fa5aad65b249da.png',
        desc: '白金卡'
      }, {
        id: 9,
        imgSrc: 'https://picbed.qunarzz.com/19b4f6d2fabd617789fa5aad65b249da.png',
        desc: '测试卡'
      }]
    }
  },
  computed: {
    pages () {
      const pages = []
      this.iconList.forEach((item, index) => {
        const page = Math.floor(index / 8)
        if (!pages[page]) {
          pages[page] = []
        }
        pages[page].push(item)
      })
      return pages
    }
  }

}
</script>

<style lang="stylus" scoped>
  .icons
    overflow: hidden
    height: 0
    padding-bottom: 50%

    .icon
      position: relative
      overflow: hidden
      float: left
      width: 25%
      padding-bottom: 25%

      .icon-img
        position: absolute
        top: 0
        left: 0
        right: 0
        bottom: .44rem
        box-sizing: border-box
        padding: .1rem

        .icon-img-content
          height: 100%
          display: block
          margin: 0 auto

      .icon-desc
        position: absolute
        height: .44rem
        line-height: .44rem
        left: 0
        right: 0
        bottom: 0
        text-align: center
</style>
