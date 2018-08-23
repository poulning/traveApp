<template>
  <div class="wrapper">
    <swiper :options="swiperOption" v-if="showSwiper">
      <swiper-slide v-for="item in list" :key="item.id"><img :src="item.imgUrl" class="swiper-img"/></swiper-slide>
      <div class="swiper-pagination"  slot="pagination"></div>
    </swiper>
  </div>
</template>
<script>
export default{
  data(){
    return {
      swiperOption: {
        loop: true,
        pagination: {
          el: '.swiper-pagination'
        },
        autoplay: true
      }
    }
  },
  props: {
    list: Array
  },
  computed: {
    showSwiper(){
      return this.list.length > 0
    }
  }
}
</script>
<style lang="stylus" scoped>
.wrapper >>> .swiper-pagination-bullet-active
  background: #fff !important
.wrapper
  overflow: hidden
  width: 100%
  height: 0
  padding-bottom: 26.66%
  background: #ccc
  .swiper-img
    width: 100%
</style>
