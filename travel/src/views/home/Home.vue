<template>
  <div class="home">
    <home-header></home-header>
    <v-swiper :swiperImgList="swiperImgList"></v-swiper>
    <icon-area :iconList="iconList"></icon-area>
  </div>
</template>

<script>
// @ is an alias to /src
import homeHeader from '@/views/home/components/homeHeader'
import vSwiper from '@/components/vSwiper'
import IconArea from '@/components/IconArea'
import dataSource from '@/assets/dataSource'

export default {
  name: 'Home',
  components: {
    homeHeader,
    [vSwiper.name]:vSwiper,
    IconArea
  },
  data () {
    return {
      swiperImgList:dataSource.swiperImgList,
      iconList: dataSource.iconList
    }
  },
}
</script>
