<template>
   <div>
    <div class='title'>热销推荐</div>
    <ul>
      <li class="item border-bottom" v-for="item in list" :key='item.id'>
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
  props: {
    list: Array
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
