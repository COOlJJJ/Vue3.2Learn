<template>
  <div>
    <h1>命名空间导入组件 一次性导入所有的</h1>
    <All.Bar />
    <All.Foo />
  </div>
</template>


<script setup lang="ts">
import * as All from "../02-01-namecomponents/components/index";
</script>

<style scoped>
</style>
