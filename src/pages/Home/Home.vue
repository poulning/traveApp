<template>
  <div>
    <home-header :city="city"></home-header>
    <home-swiper :list="swiperList"></home-swiper>
    <home-icons :list="iconList"></home-icons>
    <home-recommend :list="recommendList"></home-recommend>
    <home-weekend :list="weekendList"></home-weekend>
  </div>
</template>
<script>
import HomeHeader from '@/pages/Home/components/Header'
import HomeSwiper from '@/pages/Home/components/Swiper'
import HomeIcons from '@/pages/Home/components/Icons'
import HomeRecommend from '@/pages/Home/components/Recommend'
import HomeWeekend from '@/pages/Home/components/Weekend'
import axios from 'axios'
export default{
  data(){
    return {
      city: '',
      swiperList: [],
      iconList: [],
      recommendList: [],
      weekendList: []
    }
  },
  components: {
    HomeHeader,
    HomeSwiper,
    HomeIcons,
    HomeRecommend,
    HomeWeekend
  },
  methods: {
    getHomeData(){
      axios.get('/api/index.json').then((response) => {
        var res = response.data
        if (res.ret){
          let data = res.data
          this.city = data.city
          this.swiperList = data.swiperList
          this.iconList = data.iconList
          this.recommendList = data.recommendList
          this.weekendList = data.weekendList
        }
      })
    }
  },
  mounted(){
    this.getHomeData()
  }
}
</script>
