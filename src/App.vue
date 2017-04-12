<template>
<div id="app">
  <div class="wrapper">
    <h1 class="masked">Simon Zhang</h1>
    <h2 ref="text"></h2>
    <p><a href="./archives/">Blog</a></p>
    <p><a href="https://github.com/SimonZhangITer">GitHub</a></p>
    <p><a href="https://twitter.com/SimonZhangr">Twitter</a></p>
    <p><a href="http://weibo.com/3120797583/profile?topnav=1&wvr=6">微博</a></p>
    <p><a href="https://www.zhihu.com/people/SimonZhangR/activities">知乎</a></p>
  </div>
</div>
</template>

<script>
// let str = 'Love Code & Love Beautiful Things'
let str = 'Love Code & Love Beauty & Love Life'
let pos = 0
let len = str.length
export default {
  name: 'homepage',
  mounted() {
    this.printer()
  },
  methods: {
    printer() {
      let text = this.$refs.text
      text.innerHTML = str.substring(0, pos) + (pos >= len ? '' : "|")
      if (pos++ >= str.length) {
        return
      }
      setTimeout(() => {
        this.printer()
      }, 200);
    }
  }
}
</script>

<style lang="stylus">
$font-color = #999
#app
  font-family 'Open Sans', 'Helvetica Neue', 'Hiragino Sans GB', 'LiHei Pro', Arial, sans-serif
  color #333
  .masked{
      background-image: -webkit-linear-gradient(left, #147B96, rgba(163, 228, 208, 0.71) 25%, #147B96 50%, rgba(163, 228, 208, 0.71) 75%, #147B96);
      -webkit-text-fill-color: transparent;
      -webkit-background-clip: text;
      -webkit-background-size: 200% 100%;
      -webkit-animation: masked-animation 4s infinite linear;
  }
  @keyframes masked-animation {
      0%  { background-position: 0 0;}
      100% { background-position: -100% 0;}
  }
  .wrapper
    position absolute
    left 0
    width 320px
    text-align center
    top 50%
    left 50%
    margin-left -160px
    margin-top -160px
    user-select none
    h1
      font-size 25px
      letter-spacing 3px
    h2
      color $font-color
      font-weight normal
      font-size 14px
      letter-spacing 2px
      margin-bottom 30px
    p
      margin 0
      line-height 26px
      a
        font-size 15px
        text-decoration none
        color $font-color
        transition all .2s ease
        letter-spacing 2px
        &:hover
          color red
</style>
