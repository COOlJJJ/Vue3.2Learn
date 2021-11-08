<template>
  <div>
    <!-- 动态组件 -->
    <component :is="condition ? Bar: Foo" />
  </div>
</template>

<!-- Vue3 setup语法糖组件功能 =》 会根据Vue文件名变成组件名 不需要给组件加name 同时导入组件后可以直接使用了 很香-->
<script setup lang="ts">
import { ref } from "vue";
import Bar from "./Bar.vue";
import Foo from "./Foo.vue";

const condition = ref(false);

setTimeout(() => {
  condition.value = !condition.value;
}, 200);
</script>

<style scoped>
</style>
