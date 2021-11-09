<template>
  <div>
    <button @click="handleClick">点击触发</button>
    <div>
      点击触发 handleClick事件
      <input type="checkbox" name id @change="handleChange" />
    </div>
  </div>
</template>

<script setup lang="ts">
//注册自定义事件
//类型检查
const emits = defineEmits<{
  (e: "parentClick", data: number): void;
  (e: "parentChange"): void;
}>();

const handleClick = () => {
  //调用
  emits("parentClick", 2);
};
const handleChange = () => {
  emits("parentChange");
};
</script>

<style scoped>
</style>