<template>
  <div class="swiper-container">
    <swiper ref="mySwiper" :options="swiperOptions">
      <swiper-slide v-for="item of swiperImgList" :key="item.id">
        <img :src="item.src" />
      </swiper-slide>
      
      <div class="swiper-pagination" slot="pagination"></div>
    </swiper>
  </div>
</template>
 
<script>
  export default {
    name: 'vSwiper',
    props: ['swiperImgList'],
    data () {
      return {
        swiperOptions: {
          pagination: {
            el: '.swiper-pagination'
          },
          // Some Swiper option/callback...
          loop: true,
        }
      }
    },
    computed: {
      swiper() {
        return this.$refs.mySwiper.$swiper
      }
    },
    mounted() {
      // console.log('Current Swiper instance object', this.swiper)
      this.swiper.slideTo(3, 1000, false)
    }
  }
</script> 
<style lang="stylus" scoped>
  .swiper-container
    width : 100%
    height : 3rem
    img
      width: 100%
      height: 3rem
</style> 