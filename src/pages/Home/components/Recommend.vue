<template>
  <div>
    <h2 class="title">热门推荐</h2>
    <ul>
      <li class="item border-bottom" v-for="item in list" v-bind:key="item.id">
        <img class="item-img" :src="item.imgUrl" alt="">
        <div class="item-info">
          <h3 class="item-title">{{item.title}}</h3>
          <p class="item-desc">{{item.desc}}</p>
          <button class="item-button">查看详情</button>
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
.item
  overflow: hidden
  display: flex
  height: 1.9rem
  .item-img
    width: 1.7rem
    height: 1.7rem
    padding: .1rem
  .item-info
    flex: 1
    min-width: 0
    padding: .1rem
    .item-title
      line-height: .54rem
      font-size: .32rem
      ellipsis()
    .item-desc
      line-height: .4rem
      color: #616161
      ellipsis()
    .item-button
      margin-top: .12rem
      padding: 0 .4rem
      background: #ff9300
      color: #fff
      border-radius: .08rem
</style>
