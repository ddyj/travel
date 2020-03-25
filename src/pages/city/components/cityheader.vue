<template>
 <div class="header">
   城市选择
   <router-link to="/">
    <div class="iconfont back-cityheader">&#xe624;</div>
   </router-link>
 </div>
</template>

<script>
export default {
  name: 'cityheader'
}
</script>

<style lang="stylus" scoped>
  .header
   position: relative
   line-height: 43px
   width: 100%
   overflow: hidden
   text-align: center
   color: white
   background: #00BCD4
   font-size: 20px
   .back-cityheader
    position: absolute
    top: 0
    left: 0
    width: 32px
    text-align: center
    font-size: 20px
    color: white
</style>
