<script setup lang="ts" >
interface List {
  id: number;
  content: String;
}

// Ts声明
//运行时声明和类型声明不能同时使用
//withDefaults 设置默认值
const props = withDefaults(
  defineProps<{
    title: String;
    list: List[];
  }>(),
  {
    title: "类型声明",
    list: [
      {
        id: 3,
        content: "333"
      }
    ]
  }
);

console.log(props.title, props.list);
</script>

<template>
  <div>
    <h1>defineProps-ts</h1>
    <p>title:{{title}}</p>
    <ul>
      <li v-for="item in list" :key="item.id">{{item.content}}</li>
    </ul>
  </div>
</template>