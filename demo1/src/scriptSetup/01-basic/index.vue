<template>
  <div>
    <h1>Vue3正常语法</h1>
    {{ count }}
    <button @click="add">+</button>
  </div>
</template>
<!-- vue3 如果用ts，导出时候要用 defineComponent，这俩是配对的，为了类型的审查正确 -->
<script lang="ts">
import { defineComponent, ref } from "vue";

export default defineComponent({
  setup() {
    //ref 使其变成响应式
    const count = ref(2);

    const add = () => {
    //.value 获取其值  这边会自动提示因为有Volar
      count.value += 1;
    };
    return {
      count,
      add
    };
  },
});
</script>


<style scoped>
</style>