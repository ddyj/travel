<template>
   <div>
    <div class='title'>热销推荐</div>
    <ul>
      <li class="item border-bottom" v-for="item in recommendlist" :key='item.id'>
        <img class="item-img" :src="item.imgurl">
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
          <button class="item-button">查看详情</button>
        </div>
      </li>
    </ul>
   </div>
</template>

<script>
export default{
  name: 'homerecommend',
  data () {
    return {
      recommendlist: [{
        id: '0001',
        imgurl: 'http://img1.qunarzz.com/sight/p0/1602/53/53cf6caed9f9b9ee90.img.jpg_200x200_f5476a84.jpg',
        title: '华清宫',
        desc: '探寻杨贵妃御汤遗址'
      }, {
        id: '0002',
        imgurl: 'https://imgs.qunarzz.com/sight/p0/1411/1a/5582f9f24bc50b475a8cbda4c5ac8d24.water.jpg_200x200_a0d48950.jpg',
        title: '秦始皇陵博物院',
        desc: '发现稀世珍宝'
      }, {
        id: '0003',
        imgurl: 'https://imgs.qunarzz.com/sight/p0/1508/db/dbd0bef45fbc36b3.img.jpg_200x200_1b88abcf.jpg',
        title: '大唐芙蓉园',
        desc: '共赏唐代园林艺术'
      }, {
        id: '0004',
        imgurl: 'https://imgs.qunarzz.com/sight/p0/1706/85/8515d6b766575507a3.water.jpg_200x200_30acb7d3.jpg',
        title: '白鹿原',
        desc: '带你走进陈忠实的小说世界'
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
  .item
   touch-action: none
   overflow: hidden
   display: flex
   height: 94px
   .item-img
    width: 92px
    height: 92px
    padding: 2px
   .item-info
    flex: 1
    padding: 2px
    min-width: 0
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
    .item-button
     line-height: 20px
     margin-top: 8px
     background #ff9300
     padding: 4px
     border-radius: 3px
     overflow: hidden
     white-space: nowrap
     text-overflow: ellipsis
</style>
