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
const emits = defineEmits(["parentClick", "parentChange"]);

const handleClick = () => {
  //调用
  //emits("parentClick");

  emits("parentClick", "3"); //普通写法没有很好的类型检查
};
const handleChange = () => {
  emits("parentChange");
};
</script>

<style scoped>
</style>