<template>
  <div class="home">
    <home-header></home-header>
    <v-swiper :swiperImgList="swiperImgList"></v-swiper>
    <icon-area :iconList="iconList"></icon-area>
    <home-recommend :recommendList="recommendList"></home-recommend>
    
  </div>
</template>

<script>
// @ is an alias to /src
import homeHeader from '@/views/home/components/homeHeader'
import vSwiper from '@/components/vSwiper'
import IconArea from '@/components/IconArea'
import dataSource from '@/assets/dataSource'
import HomeRecommend from './components/homeRecommend'

export default {
  name: 'Home',
  components: {
    homeHeader,
    [vSwiper.name]:vSwiper,
    IconArea,
    [HomeRecommend.name]: HomeRecommend
  },
  data () {
    return {
      swiperImgList:dataSource.swiperImgList,
      iconList: dataSource.iconList,
      recommendList: dataSource.recommendList
    }
  },
}
</script>
