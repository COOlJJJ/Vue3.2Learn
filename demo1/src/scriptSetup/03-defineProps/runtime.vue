<script lang="ts">
export default {
  props: {
    name: String,
    age: Number
  }
};
</script>

<template>
  <div>
    <h1>Runtime</h1>
    <p>name:{{name}}</p>
    <p>age:{{age}}</p>
  </div>
</template>