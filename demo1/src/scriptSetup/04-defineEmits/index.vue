<template>
  <p>{{count}}</p>
  <!-- <Info @parentClick="parentClick" @parentChange="parentChange" /> -->
  <Infots @parentClick="parentClick"  @parentChange="parentChange" />
</template>

<script setup lang="ts">
// import Info from "./info.vue";
import Infots from "./info-ts.vue";
import { ref } from "vue";
const count = ref(1);

const parentClick = (datas: Number) => {
  alert("子组件触发了父组件的parentClick");
  count.value += datas;
};
const parentChange = () => {
  alert("子组件触发了父组件的parentChange");
};
</script>

<style scoped>
</style>