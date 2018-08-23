<template>
  <div>
    <div class="header">
      城市选择
      <router-link class="header-back" to="/">
        <span class="iconfont">&#xe624;</span>
      </router-link>
    </div>
  </div>
</template>
<script>
export default{}
</script>
<style lang="stylus" scoped>
@import '~styles/stylus/variables.styl'
.header
  overflow: hidden
  position: relative
  height: $headerheight
  line-height: $headerheight
  text-align: center
  color: #fff
  font-size: .34rem
  background: $bgcolor
  .header-back
    position: absolute
    left: 0
    top: 0
    width: .64rem
    height: 100%
    font-size: .32rem
    color: #fff
</style>
