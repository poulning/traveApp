<template>
  <div class="header">
    <div class="header-left"><span class="iconfont">&#xe624;</span></div>
    <div class="header-input">
      <span class="iconfont">&#xe632;</span>
      请选择城市/景点/游戏主题
    </div>
    <router-link class="header-right" to="/city">
      {{city}}<span class="iconfont">&#xe6a4;</span>
    </router-link>
  </div>
</template>
<script>
export default{
  props: {
    city: String
  }
}
</script>
<style lang="stylus" scoped>
@import '~styles/stylus/variables.styl'
.header
  display: flex
  height: $headerheight
  line-height: $headerheight
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
    color: #fff
</style>
