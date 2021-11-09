<script setup lang="ts">
import { ref } from "vue";
import { onMounted } from "@vue/runtime-core";
import Infots from "./info-ts.vue";


const InfoRef = ref<{ count: number; handle: () => void } | null>(null);
//父组件获取
onMounted(() => {
  console.log(InfoRef.value?.count);
  InfoRef.value?.handle();
});
</script>

<template>
  <Infots ref="InfoRef" />
</template>

<style scoped>
</style>