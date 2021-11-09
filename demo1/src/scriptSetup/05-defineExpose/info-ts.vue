<template>
  <h1>Setup</h1>
  {{count}}
</template>

<script setup lang="ts">
import { ref } from "vue";
const count = ref(2);

const handle = () => {
  console.log("这是子组件的方法");
};

//暴露子组件的方法和属性
defineExpose({
  count,
  handle
});
</script>


<style scoped>
</style>