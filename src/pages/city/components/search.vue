<template>
  <div class="search">
    <input type="text" class="search-input" placeholder="请输入城市名或拼音" />
  </div>
</template>
<script>
export default {
  name: 'CitySearch'
}
</script>
<style lang='stylus' scoped>
  @import '~styles/varibles.styl'
  .search
    height .72rem
    padding 0 .1rem
    background $bgColor
    .search-input
      height 0.62rem
      width 100%
      box-sizing border-box
      padding 0 .1rem
      text-align center
      line-height .62rem
      border-radius .06rem
      color #666
</style>
