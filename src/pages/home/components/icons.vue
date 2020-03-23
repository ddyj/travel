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
  data: function () {
    return {
      swiperOptions: {
        loop: false
      },
      iconlist: [{
        id: '0001',
        imgurl: 'https://imgs.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
        desc: '景点门票'
      }, {
        id: '0002',
        imgurl: 'https://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20193/f0f00d6dfe038c044dbc9a437f58b0eb.png',
        desc: '一日行'
      }, {
        id: '0003',
        imgurl: 'https://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20194/5ea666792b98f34c86faea912b5fbcf9.png',
        desc: '玩转周边'
      }, {
        id: '0004',
        imgurl: 'https://imgs.qunarzz.com/piao/fusion/1803/20/831d62d2e1c7be02.png',
        desc: '华清宫'
      }, {
        id: '0005',
        imgurl: 'https://imgs.qunarzz.com/piao/fusion/1804/ff/fdf170ee89594b02.png',
        desc: '西安必玩'
      }, {
        id: '0006',
        imgurl: 'https://imgs.qunarzz.com/piao/fusion/1803/fa/2548667cb6e902.png',
        desc: '动植物园'
      }, {
        id: '0007',
        imgurl: 'https://imgs.qunarzz.com/piao/fusion/1803/ab/6f7d6e44963c9302.png',
        desc: '泡温泉'
      }, {
        id: '0008',
        imgurl: 'https://imgs.qunarzz.com/piao/fusion/1803/fa/2548667cb6e902.png',
        desc: '兵马俑'
      }, {
        id: '0009',
        imgurl: 'https://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20196/9c76635f623759e3db287c4850fcb0a5.png',
        desc: '华山'
      }, {
        id: '0010',
        imgurl: 'https://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20196/9c76635f623759e3db287c4850fcb0a5.png',
        desc: '芙蓉园'
      }]
    }
  },
  // 分页算法原理 每次计算一次page 前8个数(数组编号0~7)对应page=0,检测到if (!pages[page])时，新建一个空数组，从新输入(形成新页面)
  computed: {
    pages: function () {
      const pages = []
      this.iconlist.forEach((item, index) => {
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
