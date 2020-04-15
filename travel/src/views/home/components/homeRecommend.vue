<template>
  <div class="home-recommend">
    <div class="title">
      <p>热门推荐</p>
    </div>
    <div v-for="item of recommendList" :key="item.id">
      <van-card
        :tag="item.tag"
        :price="item.price"
        :desc="item.desc"
        :title="item.title"
        :thumb="item.thumb"
        :origin-price="item.originPrice"
      >
        <template #tags>
          <van-tag plain type="danger">hot</van-tag>
          <van-tag plain type="danger">cool</van-tag>
        </template>
        
      </van-card>
    </div>
  </div>
  
</template>>
<script>
import {Card,Button,Tag} from 'vant'

export default {
  name:'HomeRecommend',
  props: ['recommendList'],
  components:{
    [Card.name]: Card,
    [Button.name]: Button,
    [Tag.name]: Tag
  }
  
}
</script>>
<style lang="stylus" scoped>
.van-card__title
  font-size .28rem
.title
  background-color #ccc
  color #333
  height .6rem
  padding-left 0.4rem
  display flex
  align-items center
  p
    font-size 0.28rem
</style>