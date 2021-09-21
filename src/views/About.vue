<template>
  <h1>About!!</h1>
  <router-link to="/">Go to home</router-link>
  <p>数字a</p>
  <span>{{ a }}</span>
  <p>数字b</p>
  <span>{{ b }}</span>
</template>

<script setup>
  import {  ref } from "vue";
  const a = 1
  const b = ref(2)

  defineExpose({
    a,
    b
  })
</script>