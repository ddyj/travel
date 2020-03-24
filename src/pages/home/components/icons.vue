<template>
  <div class="icons">
    <swiper ref="mySwiper" :options="swiperOptions">
    <swiper-slide v-for="(page,index) in pages" :key="index">
    <div class="icon" v-for="item in page" :key="item.id">
      <div class="icon-img">
        <img class="icon-img-content" :src="item.imgurl">
      </div>
      <p class="icon-desc">{{item.desc}}</p>
    </div>
    </swiper-slide>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'homeicons',
  props: {
    list: Array
  },
  data: function () {
    return {
      swiperOptions: {
        loop: false
      }
    }
  },
  // 分页算法原理 每次计算一次page 前8个数(数组编号0~7)对应page=0,检测到if (!pages[page])时，新建一个空数组，从新输入(形成新页面)
  computed: {
    pages: function () {
      const pages = []
      this.list.forEach((item, index) => {
        const page = Math.floor(index / 8)
        if (!pages[page]) {
          pages[page] = []
        }
        pages[page].push(item)
      })
      return pages
    }
  }
}
</script>

<style lang="stylus" scoped>
  .icons >>> .swiper-container
   width: 100%
   overflow: hidden
   height: 0
   padding-bottom: 50%
   background: white
  .icons
   margin-top: 3px
   .icon
    position: relative
    overflow: hidden
    float: left
    width: 25%
    height: 0
    padding-bottom: 25%
    background: white
    .icon-img
     position: absolute
     top: 0
     left: 0
     right: 0
     bottom: 22px
     box-sizing: border-box
     padding: 1px
     background: white
     .icon-img-content
      display: block
      margin: 0 auto
      height: 100%
    .icon-desc
     position: absolute
     left: 0
     right: 0
     bottom: 0
     height: 22px
     line-height: 22px
     text-align: center
     color: #333
     overflow: hidden
     white-space: nowrap
     text-overflow: ellipsis

</style>
