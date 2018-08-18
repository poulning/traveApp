<template>
  <div class="header">
    <div class="header-left"><span class="iconfont">&#xe624;</span></div>
    <div class="header-input">
      <span class="iconfont">&#xe632;</span>
      请选择城市/景点/游戏主题
    </div>
    <div class="header-right">城市<span class="iconfont">&#xe6a4;</span></div>
  </div>
</template>
<script>
export default{}
</script>
<style lang="stylus" scoped>
@import '~@/assets/styles/stylus/variables.styl'
.header
  display: flex
  height: .86rem
  line-height: .86rem
  background: $bgcolor
  color: #fff
  .header-left
    width: .64rem
    float: left
    text-align: center
  .header-input
    flex: 1
    height: .64rem
    line-height: .64rem
    margin-top: .12rem
    padding-left: .2rem
    background: #fff
    color: #ccc
    border-radius: .1rem
  .header-right
    float: right
    width: 1.24rem
    text-align: center
</style>
