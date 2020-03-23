<template>
   <div>
    <div class='title'>周末去哪</div>
    <ul>
      <li class="item border-bottom" v-for="item in recommendlist" :key='item.id'>
        <div class="item-img-wrapper">
         <img class="item-img" :src="item.imgurl">
        </div>
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
        </div>
      </li>
    </ul>
   </div>
</template>

<script>
export default{
  name: 'homeweekend',
  data () {
    return {
      recommendlist: [{
        id: '0001',
        imgurl: 'https://imgs.qunarzz.com/sight/source/1505/19/58f233e11df7ef.jpg_r_640x214_6b42c9fc.jpg',
        title: '西安必打卡',
        desc: '寻长安梦，开启穿越的圆梦之旅'
      }, {
        id: '0002',
        imgurl: 'https://imgs.qunarzz.com/sight/source/1811/63/808c022b285a2c.jpg_r_640x214_ad984479.jpg',
        title: '探寻文化古都',
        desc: '寻长安梦，开启穿越的圆梦之旅'
      }, {
        id: '0003',
        imgurl: 'https://imgs.qunarzz.com/sight/source/1507/de/e6ba44d61894c0.jpg_r_640x214_847324d0.jpg',
        title: '西安演出在线',
        desc: '这里有绚丽奇幻的神秘梦幻舞剧，歌舞揭开盛唐面纱，体验穿越时空的奇妙，感受大唐之盛世'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>

.title
   touch-action: none
   margin-top: 4px
   line-height: 30px
   background: #E5E5E5
   text-indent: 4px
   font-weight: 400
  .item-img-wrapper
   overflow: hidden
   height: 0
   padding-bottom: 33.9%
   .item-img
    width: 100%
  .item-info
    padding: 2px

    .item-title
     line-height: 35px
     font-size: 16px
     color: #000000
     overflow: hidden
     white-space: nowrap
     text-overflow: ellipsis
    .item-desc
     line-height: 16px
     color: #969896
     overflow: hidden
     white-space: nowrap
     text-overflow: ellipsis
</style>
