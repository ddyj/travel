<template>
 <ul class="list">
   <li class="item">A</li>
   <li class="item">A</li>
   <li class="item">A</li>
   <li class="item">A</li>
   <li class="item">A</li>
   <li class="item">A</li>
   <li class="item">A</li>
   <li class="item">A</li>
 </ul>
</template>

<script>
export default {
  name: 'Alphabet'
}
</script>

<style lang="stylus" scoped>
  .list
   display: flex
   flex-direction: column
   justify-content: center
   position: absolute
   top: 79px
   right: 0
   bottom: 0
   width: 20px
   .item
    text-align: center
    line-height: 20px
    color: #00BCD4
</style>
