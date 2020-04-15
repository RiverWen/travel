<template>
  <div class="icon-area-container">
    <swiper>
      <swiper-slide v-for="(page,index) of pages" :key="index">
        <div class="page-container">
          <div class="icon-container" v-for="item of page" :key="item.id">
            <img :src="item.src" :alt="item.desc"/>
            <div class="desc-container">
              <p>{{item.desc}}</p>
            </div>
          </div>
        </div>
      </swiper-slide>
    </swiper>
  </div>
</template>
 
<script>
  export default {
    name: 'IconArea',
    props: ['iconList'],
    data () {
      return {
      }
    },
    computed: {
      pages () {
        let pages = []
        let perPage = 8
        if(this.iconList.length){
          this.iconList.forEach((element,index) => {
            let page = Math.floor( index / perPage)
            if(!pages[page]){
              pages[page] = []
            }
            pages[page].push(element)
          })
        }
        return pages
      },
    },
  }
</script> 

<style lang="stylus" scoped>
@import '~@/assets/mixins.styl'
  .page-container
    display flex
    flex-wrap wrap
    overflow hidden
    height 4rem
    .icon-container
      display flex
      flex-direction column
      align-items center
      width 25%
      height 2rem
      img 
        width 1.4rem
        margin-top 0.05rem
      .desc-container
        width 80%
        p
          line-height 0.5rem
          text-align center
          color #333
          ellipsis()
</style> 