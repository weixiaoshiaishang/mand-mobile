<template>
  <div class="characteristic-card">
    <img :src="icon" :alt="title">
    <div class="characteristic-text">
      <h2 class="characteristic-title">{{title}}</h2>
      <p class="characteristic-describe">{{describe}}</p>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    icon: {
      type: String
    },
    title: {
      type: String
    },
    describe: {
      type: String
    },
  },
}
</script>

<style lang="stylus">
.characteristic-card
  display flex
  align-items center
  width 590px
  height 210px
  padding 0 46px
  background-color: rgba(255,255,255,.8)
  border 2px solid #FFF
  border-radius 16px
  box-sizing border-box
  transition background-color .3s

  &:hover
    background-color: #FFF

  img
    width 120px
    height 120px
    margin-right 33px

  .characteristic-title
    height 35px
    margin-bottom 34px
    line-height 35px
    font-size 30px
    font-weight normal
    color #061A33

  .characteristic-describe
    font-size 20px
    line-height 23px
    color #061A33

@media (max-width: 750px)
  .characteristic-card
    width 6.7rem
    height 2.24rem
    padding 0 .48rem
    border-radius .32rem

    img
      width 1.4rem
      height 1.4rem
      margin-right .36rem

    .characteristic-title
      height .36rem
      margin-bottom .26rem
      line-height .36rem
      font-size .32rem

    .characteristic-describe
      font-size .26rem
      line-height .32rem
</style>
