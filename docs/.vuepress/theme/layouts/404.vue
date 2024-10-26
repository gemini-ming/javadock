<template>
  <div class="theme-container">
    <div class="theme-vdoing-content">
      <span> <img :src="getRandomImage()" alt="Random Image" class="random-image" /></span>
      <blockquote>{{ getMsg() }}</blockquote>
      <router-link to="/">返回首页</router-link>
    </div>
  </div>
</template>

<script>
// 随机文字
const msgs = [
  `文档暂时还在编写中`,
  `作者熬夜编写文档中`,
  `文档快马加鞭接入中`,
  `文档正在飞速接入中`
]

// 随机图片路径
const imgPaths = [
  '/img/404page/404-error.png',
  '/img/404page/404.png',
  '/img/404page/404-error.png',
  '/img/404page/404-error.png'
]

export default {
  methods: {
    getMsg () {
      return msgs[Math.floor(Math.random() * msgs.length)]
    },
    getRandomImage () {
      return imgPaths[Math.floor(Math.random() * imgPaths.length)]
    }
  }
}
</script>

<style lang="stylus" scoped>
.theme-vdoing-content
  margin 3rem auto
  padding 1.5rem
  text-align center
  span
    font-size 6rem
    color $accentColor

.random-image
  margin-top 2rem
  width 300px
  height auto
</style>
