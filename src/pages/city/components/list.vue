<template>
  <div class="list" ref="wrapper">
    <div>
    <div class="area">
      <div class="title border-topbottom">当前城市</div>
      <div class="buttonlist">
        <div class="button-wrapper">
          <div class="button">西安</div>
        </div>
      </div>
    </div>
    <div class="area">
      <div class="title border-topbottom">热门城市</div>
      <div class="buttonlist">
        <div class="button-wrapper">
          <div class="button">西安</div>
        </div>
        <div class="button-wrapper">
          <div class="button">西安</div>
        </div>
        <div class="button-wrapper">
          <div class="button">西安</div>
        </div>
        <div class="button-wrapper">
          <div class="button">西安</div>
        </div>
        <div class="button-wrapper">
          <div class="button">西安</div>
        </div>
        <div class="button-wrapper">
          <div class="button">西安</div>
        </div>
      </div>
    </div>
    <div class="area">
      <div class="title border-topbottom">A</div>
      <div class="item-list">
        <div class="item border-bottom">阿拉尔</div>
        <div class="item border-bottom">阿拉尔</div>
        <div class="item border-bottom">阿拉尔</div>
        <div class="item border-bottom">阿拉尔</div>
        <div class="item border-bottom">阿拉尔</div>
        <div class="item border-bottom">阿拉尔</div>
        <div class="item border-bottom">阿拉尔</div>
        <div class="item border-bottom">阿拉尔</div>
      </div>
    </div>
    <div class="area">
      <div class="title border-topbottom">B</div>
      <div class="item-list">
        <div class="item border-bottom">阿拉尔</div>
        <div class="item border-bottom">阿拉尔</div>
        <div class="item border-bottom">阿拉尔</div>
        <div class="item border-bottom">阿拉尔</div>
        <div class="item border-bottom">阿拉尔</div>
        <div class="item border-bottom">阿拉尔</div>
        <div class="item border-bottom">阿拉尔</div>
        <div class="item border-bottom">阿拉尔</div>
      </div>
    </div>
    <div class="area">
      <div class="title border-topbottom">C</div>
      <div class="item-list">
        <div class="item border-bottom">阿拉尔</div>
        <div class="item border-bottom">阿拉尔</div>
        <div class="item border-bottom">阿拉尔</div>
        <div class="item border-bottom">阿拉尔</div>
        <div class="item border-bottom">阿拉尔</div>
        <div class="item border-bottom">阿拉尔</div>
        <div class="item border-bottom">阿拉尔</div>
        <div class="item border-bottom">阿拉尔</div>
      </div>
    </div>
    </div>
  </div>
</template>

<script>
import Bscroll from 'better-scroll'
export default {
  name: 'list',
  mounted: function () {
    this.scroll = new Bscroll(this.$refs.wrapper)
  }
}
</script>

<style lang="stylus" scoped>
  .border-topbottom
   &:before
    border-color: #CCCCCC
   &:after
    border-color: #CCCCCC
  .border-bottom
   &:before
    border-color: #CCCCCC
  .list
   overflow: hidden
   position: absolute
   top: 79px
   left:0
   right:0
   bottom:0
  .title
    line-height: 27px
    font-size: 13px
    background: #EEEEEE
    padding-left: 10px
    color: #666666
  .buttonlist
    overflow: hidden
    padding: 5px 3px 5px 5px
    .button-wrapper
     float: left
     width: 33.33%
     .button
      margin: 5px
      padding: 5px 0
      text-align: center
      border: 1px solid #CCCCCC
      border-radius: 3px
  .item-list
    .item
     line-height: 37px
     color: #666666
     padding-left: 10px
</style>
