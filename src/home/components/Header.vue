<template>
  <div class="header">
    <div class="header-left">
      <div class="iconfont back-iconfont">&#xe624;</div>
    </div>
    <div class="header-input">
      <span class="iconfont input-iconfont">&#xe632;</span>
      输入城市/景点/游玩主题
    </div>
    <div class="header-right">
      城市
      <span class="iconfont">&#xe64a;</span>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HomeHeader'
}
</script>

<style lang="stylus" scoped>
  @import '~styles/varibles.styl'
  .header
    display flex
    line-height .86rem
    background $bgColor
    color: #fff
    .header-left
      width: .64rem
      float: left
      .back-iconfont
        text-align: center
        font-size: .4rem
    .header-input
      flex: 1
      height: .64rem
      line-height: .64rem
      margin-top: .12rem
      margin-left: .2rem
      border-radius: .1rem
      background: #fff
      color: #ccc
      .input-iconfont
        margin-left: .2rem
    .header-right
      width: 1.24rem
      float: right
      text-align: center
</style>
