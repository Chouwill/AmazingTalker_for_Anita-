<template>
  <div>字數:{{msgCount}}</div>
  data: {{ data }}
</template>

<script setup>
import { computed, watch } from "vue";

// const emit = defineEmits(['updatae'])



// watch(msgCount, (newValue)=>{
//     emit('updatae',`from child: ${newValue}`)
// })

// ---------------------------------------------------
const props = defineProps({
  data: {
    type: String,
    default: "",
  },
});
const msgCount = computed(() => {
  return props.data.length;
});
</script>

<style scoped></style>
