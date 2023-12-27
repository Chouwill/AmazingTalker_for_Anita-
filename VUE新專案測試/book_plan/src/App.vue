<template>
  <div class="warp">
    <Header />
    <!--  冒出紅色 ?????   -->
    <Child />
    <Main />
    <Footer />
  </div>
</template>

<script setup>
import Header from "./components/Header.vue";
import Child from "./components/Child.vue";
import Main from "./components/Main.vue";
import Footer from "./components/Footer.vue";
</script>

<style scoped>
*_ {
  margin: 0;
  padding: 0;
  list-style: none;
}
.warp {
  width: 1000px;
  margin: 0 auto;
  border: 5px solid yellow;
}
</style>
