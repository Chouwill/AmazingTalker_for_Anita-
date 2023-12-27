<template>
  <input type="text" v-model="msg" />
  <br />

  <Child :data="msg" @updatae="updateHandler" />
</template>

<script setup>
import { ref } from "vue";
import Child from "./components/Child.vue";

const msg = ref("");
// const updateHandler = (data) => {
//   console.log(data);
// };
</script>

<style scoped></style>
