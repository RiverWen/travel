<template>
  <div class="home">
    <home-header></home-header>
    <v-swiper :swiperImgList="swiperImgList"></v-swiper>
  </div>
</template>

<script>
// @ is an alias to /src
import homeHeader from '@/views/home/components/homeHeader'
import vSwiper from '@/components/vSwiper'

export default {
  name: 'Home',
  components: {
    homeHeader,
    [vSwiper.name]:vSwiper
  },
  data () {
    return {
      swiperImgList:[
          {
            id:1,
            src:'http://img1.qunarzz.com/sight/p0/2003/de/de11d542e3f0776da3.water.jpg_600x330_d4c127a5.jpg'
          },
          {
            id:2,
            src:'http://img1.qunarzz.com/sight/p0/1803/c4/c42248b5b4bb1258a3.water.jpg_600x330_3ed6fb45.jpg'
          }
      ],
    }
  }
}
</script>
