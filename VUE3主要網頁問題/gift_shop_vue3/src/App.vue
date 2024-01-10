<template>
  <div class="wrap">
    <Header />
  </div>
</template>

<script setup>
import Header from "./components/Header.vue";
</script>

<style scoped>
 * {
        margin: 0;
        padding: 0;
        list-style: none;
        text-decoration: none;
        box-sizing: border-box;
      }
      .wrap {
        max-width: 1200px;
        border: 2px solid yellowgreen;
        margin: 0 auto;
      }


      /* 問題提問
         1.目前專案導入VUE3都會跑版
         2.是否要在網頁再包一層.wrap
         3.https://zh.wix.com/website-template/view/html/3212?originUrl=https%3A%2F%2Fzh.wix.com%2Fwebsite%2Ftemplates&tpClick=view_button&esi=b3c20a59-dda0-4641-bf36-dee166ca72c6 是否要再包一層.wrap ，寬度要設多少
        4.           */

</style>
