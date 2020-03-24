<template>
  <div class="header">
   <div class="header-left">
     <div class="iconfont back-iconfont">&#xe624;</div>
   </div>
   <div class="header-input">
     <span  class="iconfont">&#xe632;</span>
     输入城市景点游玩主题
   </div>
   <div class="header-right">
     {{this.city}}
     <span  class="iconfont arrow-iconfont">&#xe62d;</span>
   </div>
  </div>
</template>

<script>
export default {
  name: 'homeheader',
  props: {
    city: String
  }
}
</script>

<style lang="stylus" scoped>
  .header
     touch-action: none
     display: flex
     line-height: 43px
     background: #00bcd4
     color #fff
     .header-left
      width: 32px
      float: left
      .back-iconfont
       text-align: center
       font-size: 20px
     .header-input
      flex: 1
      height: 31px
      line-height: 31px
      margin-top: 6px
      margin-left: 1px
      padding-left: 10px
      background: #fff
      border-radius: 0.5px
      color: #ccc
     .header-right
      width: 62px
      float: right
      text-align: center
      .arrow-iconfont
       margin-left:-2px
       font-size: 12px
</style>
