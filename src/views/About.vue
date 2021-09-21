<script setup>
  import Test from '../components/Test.vue'
  import Slot from '../components/Slot.vue'
  import { ref } from "vue";
  import { reduce } from '../reduce'


  const a = 1
  const b = ref(2)
  const count = ref(0)


  const handleCountAdd = () => {
    count.value += 1
  }

  const handleCountReduce = () => {
    count.value = reduce(count.value)
  }

  defineExpose({
    a,
    b,
    count,
    handleCountAdd,
    handleCountReduce
  })
</script>


<template>
<h1>About!!</h1>
<router-link to="/">Go to home</router-link>
<Test foo="aaa" />
<Slot>
  aiueoao
</Slot>
<p>数字a</p>
<span>{{ a }}</span>
<p>数字b</p>
<span>{{ b }}</span>
<p>数字count</p>
<span>{{ count }}</span>
<button @click="count++">count ++</button>
<button @click="handleCountAdd">handleCountAdd</button>
<button @click="handleCountReduce">handleCountReduce</button>
</template>

