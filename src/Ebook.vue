<template>
  <div>
    <a href="./assets/test.epub">xxxxx</a>
  </div>
</template>

<script>
  import Epub from 'epubjs'
  const DOWNLOAD_URL = './assets/test.epub'
  export default {
    name: "Ebook",
    methods: {
      // 电子书的解析和渲染
      showEpub() {
        // 生成 Ebook
        this.book = new Epub(DOWNLOAD_URL)
        console.log(this.book);
        // 生成 Rendtion
        // 通过 Rendtion.display 渲染电子书

      }

    },
    mounted() {
      this.showEpub()
    }

  }
</script>

<style scoped lang="sass">
  @import "assets/styles/global"

</style>