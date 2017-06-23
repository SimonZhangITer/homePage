<template>
  <main class="container">
    <section class="content">
      <h1 class="masked">Simon Zhang</h1>
      <p>Web Front End Engineer</p>
      <a href="./archives/" title="Blog" class="blog">Blogs</a>
    </section>
    <div class="footer">
      <a href="https://github.com/SimonZhangITer" target="_blank"><i class="iconfont icon-github"></i></a>
      <a href="https://twitter.com/SimonZhangr" target="_blank"><i class="iconfont icon-twitter"></i></a>
      <a href="http://weibo.com/simonzhangr" target="_blank"><i class="iconfont icon-weibo"></i></a>
      <a href="https://www.zhihu.com/people/SimonZhangR" target="_blank"><i class="iconfont icon-zhihu_circle"></i></a>
    </div>
  </main>
</template>

<script>
import 'font-awesome/css/font-awesome.min.css'

export default {
  name: 'homepage'
}
</script>

<style lang="stylus">
$font-color = #999
body
  position absolute
  height 100%
  width 100%
  margin 0
.container
  display flex
  height: 100%;
  padding: 0;
  margin: 0;
  align-items: center;
  justify-content: center;
  font-family 'Helvetica Neue', Arial, sans-serif
  color #333
  background-color #f9f9f9
  .content
    position relative
    text-align center
    user-select none
    h1
      color: #21211f;
      font-size: 8rem;
      padding: 0;
      margin 0
      letter-spacing: -0.5rem;
      // font-family: "Gotham Narrow SSm A", "Gotham Narrow SSm B";
      font-style: normal;
      font-weight: 500;
    p
      position absolute
      margin-top -27px
      color: #21211f;
      font-size: 1.2rem;
      letter-spacing: 0.135rem;
      padding: 0 0 0 365px
      // font-family: "Sentinel A", "Sentinel B";
      font-style: normal;
      font-weight: 400;
    .blog
      position relative
      float left
      margin-top -20px
      // font-family: "Gotham Narrow SSm A", "Gotham Narrow SSm B";
      font-weight: 500;
      background: #e22a25;
      border-radius: 50px;
      padding: 0.75rem 1.5rem;
      font-size: 0.9rem;
      letter-spacing: 0.4rem;
      text-transform: uppercase;
      color: #fff;
      transition: all 0.5s ease;
      text-decoration none
      &:hover
        background: #21211f;
	      transition: all 0.5s ease;
  .footer
    position absolute
    left 0
    right 0
    bottom 35px
    text-align center
    a
      padding: 0 0.5rem;
      color: #21211f;
      font-size: 30px;
      transition: all 0.5s ease;
      cursor pointer
      text-decoration none
      .iconfont
        font-size inherit
        transition: all 0.5s ease;
      .icon-github:hover
      	color: #92928f;
      .icon-twitter:hover
      	color: #1da1f2;
      .icon-weibo:hover
      	color: #e6162d;
      .icon-zhihu_circle:hover
      	color: #0f88eb;

/***** Responsiveness *****/
@media all and (max-width: 740px)
	html, body
		font-size: 10px;

	main.container section.content
    .blog
      margin: 40px auto;
      display: block;
      padding: 1.35rem 1.5rem;
      font-size: 1.4rem;
      float none
    p
      padding: 0 0 0 228px;
      margin-top -16px

@media all and (max-width: 440px)
	html, body
		font-size: 8px;
	main.container section.content
   .blog
      margin: 40px auto;
      display: block;
      padding: 1.25rem 1.5rem;
      font-size: 1.6rem;
      float none
    p
      padding: 0 0 0 183px;
      letter-spacing: 0px;
      margin-top: -14px;
      font-size 12px
	.footer a
		font-size: 25px;

@media all and (max-width: 348px)
	html, body
		font-size: 8px;
	main.container section.content
   h1
      font-size 7rem
   .blog
      margin: 30px;
      display: block;
      padding: 1rem 1rem;
      font-size: 1.6rem;
      float none
    p
      padding: 0 0 0 156px;
      letter-spacing: 0px;
      margin-top: -13px;
      font-size 11px
	.footer a
		font-size: 25px;
</style>
