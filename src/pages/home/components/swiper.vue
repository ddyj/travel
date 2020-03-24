<template>
 <div class="wrapper">
   <swiper ref="mySwiper" :options="swiperOptions" v-if="list.length"><!-- v-if:判断返回数组是否为空，避免出现首页图为第四张图的bug -->
      <swiper-slide v-for="item in list" :key="item.id">
         <img class="swiper-image" :src="item.imgurl">
      </swiper-slide>
      <!-- 显示分页效果-->
      <div class="swiper-pagination" slot="pagination"></div>
   </swiper>
 </div>
</template>

<script>
export default {
  name: 'homeswiper',
  props: {
    list: Array
  },
  data: function () {
    return {
      swiperOptions: {
        pagination: '.swiper-pagination',
        loop: true
      }
    }
  }
}
</script>

<style lang="stylus" scoped>
  .wrapper >>> .swiper-pagination-bullet-active
    background: #fff
  .wrapper
   touch-action: none
   overflow: hidden
   width: 100%
   height: 0
   padding-bottom: 38%
   background #eee
   .swiper-image
     width: 100%
</style>
