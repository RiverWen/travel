<template>
  <div class="header">
      <div class="header-left">
        <i class="iconfont iconback"></i>
      </div>
      <div class="header-input">
        <i class="iconfont iconsearch"></i>
        输入城市/景点/游玩主题
      </div>
      <div class="header-right">
        城市
        <i class="iconfont iconarrow"></i>
      </div>
  </div>
</template>

<script>
// @ is an alias to /src

export default {
  name: 'homeHeader'
}
</script>
<style lang="stylus" scoped>
@import '~@/assets/varibles.styl'
  .header
    display: flex
    align-items : center
    line-height : 0.86rem
    background-color : $bgColor
    color : #fff
    .header-left
      width : 0.64rem
      text-align :center
      .iconback
        font-size: 0.4rem
    .header-input
      flex : 1
      background-color : #fff
      height : .64rem
      line-height : .64rem
      padding:0 .1rem
      border-radius : .1rem
      margin-left : .2rem
      color : #ccc
    .header-right
      width : 1.24rem
      text-align : center
</style>
