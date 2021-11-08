<template>
  <div>
    <h1>Setup语法糖</h1>
    {{ count }}
    <button @click="add">+</button>
  </div>
</template>

<!-- <script setup> 中的代码会在每次组件实例被创建的时候执行 -->
<!-- 不再需要使用 return 导出 -->
<script setup lang="ts">
import { ref } from "vue";

const count = ref(1);
const add = () => {
  //.value 获取其值  这边会自动提示因为有Volar
  count.value += 1;
};
</script>

<style scoped>
</style>
