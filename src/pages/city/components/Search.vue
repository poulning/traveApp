<template>
  <div class="search">
    <input class="search-input" type="text" placeholder="输入城市名或拼音">
  </div>
</template>
<scrirpt>
export default{}
</scrirpt>
<style lang="stylus" scoped>
@import '~styles/stylus/variables.styl'
.search
  height: .72rem
  padding: 0 .1rem
  background: $bgcolor
  .search-input
    box-sizing: border-box
    width: 100%
    height: .62rem
    padding: 0 .1rem
    line-height: .62rem
    background: #fff
    color: #666
    border-radius: .1rem
</style>
