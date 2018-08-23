<template>
  <div class="icons">
    <swiper class="icons-swiper" :options="swiperOption">
      <swiper-slide v-for="(page, index) in pages" v-bind:key="index">
        <div class="icon" v-for="item in page" v-bind:key="item.id">
          <div class="icon-img">
            <img class="icon-img-content" :src="item.imgUrl" alt="">
          </div>
          <p class="icon-desc">{{item.desc}}</p>
        </div>
      </swiper-slide>
      <div class="swiper-pagination"  slot="pagination"></div>
    </swiper>
  </div>
</template>
<script>
export default{
  data(){
    return {
      swiperOption: {
        pagination: {
          el: '.swiper-pagination'
        }
      }
    }
  },
  props: {
    list: Array
  },
  computed: {
    pages(){
      const pages = []
      this.list.forEach(function(item, index){
        const page = Math.floor(index / 8)
        if (!pages[page]) pages[page] = []
        pages[page].push(item)
      })
      return pages
    }
  }
}
</script>
<style lang="stylus" scoped>
.icons >>> .icons-swiper
   height: 0
   padding-bottom: 40%
  .icon
    overflow: hidden
    position: relative
    width: 25%
    float: left
    padding-bottom: 20%
    .icon-img
      position: absolute
      left: 0
      top: 0
      right: 0
      bottom: .4rem
      padding: .1rem
      box-sizing: border-box
      .icon-img-content
        display: block
        height: 100%
        margin: 0 auto
  .icon-desc
    position: absolute
    left: 0
    right: 0
    bottom: 0
    height: .4rem
    text-align: center
    color: #333
</style>
