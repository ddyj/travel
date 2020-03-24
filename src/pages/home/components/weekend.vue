<template>
   <div>
    <div class='title'>周末去哪</div>
    <ul>
      <li class="item border-bottom" v-for="item in list" :key='item.id'>
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
  props: {
    list: Array
  }
}
</script>

<style lang="stylus" scoped>

.title
   touch-action: none
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
