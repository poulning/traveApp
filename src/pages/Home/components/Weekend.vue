<template>
  <div>
    <h2 class="title">周末去哪儿</h2>
    <ul>
      <li class="item" v-for="item in list" v-bind:key="item.id">
        <div class="img-wrapper">
          <img class="item-img" :src="item.imgUrl" alt="">
        </div>
        <div class="item-info">
          <h3 class="item-title">{{item.title}}</h3>
          <p class="item-desc">{{item.desc}}</p>
        </div>
      </li>
    </ul>
  </div>
</template>
<script>
export default{
  props: {
    list: Array
  }
}
</script>
<style lang="stylus" scoped>
@import '~styles/stylus/mixins.styl'
.title
  height: .8rem
  line-height: .8rem
  background: #eee
  text-indent: .2rem
.img-wrapper
  overflow: hidden
  height: 0
  padding-bottom: 37.33%
  .item-img
    width: 100%
.item-info
  padding: .2rem
  .item-title
    line-height: .48rem
    font-size: .28rem
    color: #212121
    ellipsis()
  .item-desc
    line-height: .34rem
    font-size: .24rem
    color: #616161
    ellipsis()
</style>
