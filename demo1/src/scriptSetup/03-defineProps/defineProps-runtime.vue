<script lang="ts" setup>
// 运行时声明
defineProps({
  title: { type: String, required: true },
  list: {
    type: Array,
    required: true
  }
});
</script>

<template>
  <div>
    <h1>defineProps-runtime</h1>
    <p>title:{{title}}</p>
    <ul>
      <li v-for="item in list" :key="item.id">{{item.content}}</li>
    </ul>
  </div>
</template>