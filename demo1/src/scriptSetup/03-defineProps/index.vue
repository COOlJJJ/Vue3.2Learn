<script setup lang="ts">
import Runtime from "./runtime.vue";
import RefinePropsRuntime from "./defineProps-runtime.vue";
import RefinePropsTs from "./defineProps-ts.vue";

const list = [
  {
    id: 1,
    content: "11"
  },
  {
    id: 2,
    content: "222"
  }
];
</script>


<template>
    <Runtime name="xiaochen" :age="18" />
    <RefinePropsRuntime title="RefinePropsRuntime" :list="list" />
    <RefinePropsTs title="RefinePropsTs" :list="list" />
</template>