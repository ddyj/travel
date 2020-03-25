<template>
  <div class="search">
    <input type="text" class="search-input" placeholder="输入城市名或拼音" />
  </div>
</template>

<script>
export default {
  name: 'search'
}
</script>

<style lang="stylus" scoped>
  .search
   height: 36px
   width: 100%
   background: #00BCD4
   .search-input
    box-sizing: border-box
    width: 100%
    height: 31px
    line-height: 31px
    border: #00BCD4
    padding: 0 0.5px
    text-align: center
    color: #666666
</style>
