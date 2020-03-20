<template>
 <div class="wrapper">
   <swiper ref="mySwiper" :options="swiperOptions">
      <swiper-slide v-for="item in swiperlist" :key="item.id">
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
  data: function () {
    return {
      swiperOptions: {
        pagination: '.swiper-pagination',
        loop: true
      },
      swiperlist: [{
        id: '0001',
        imgurl: 'https://imgs.qunarzz.com/piao/fusion/1508/b2/ed1db0c917e3a3.jpg_890x330_ac9dae24.jpg',
        message: '陕西历史博物馆'
      }, {
        id: '0002',
        imgurl: 'https://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20193/cf57870ce7c3a5bd152f047221dc29f3.jpg_890x330_19ff4745.jpg',
        message: '华清宫'
      },
      {
        id: '0003',
        imgurl: 'https://imgs.qunarzz.com/piao/fusion/1709/e9/8511dbadf373b602.jpg_890x330_dc804b61.jpg',
        message: '陕西大明宫'
      }, {
        id: '0004',
        imgurl: 'https://imgs.qunarzz.com/piao/fusion/1507/29/46d244176c9623.jpg_890x330_db953c72.jpg',
        message: '兵马俑'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  .wrapper >>> .swiper-pagination-bullet-active
    background: #fff
  .wrapper
   overflow: hidden
   width: 100%
   height: 0
   padding-bottom: 38%
   background #eee
   .swiper-image
     width: 100%
</style>
