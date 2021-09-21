<template>
  <h1>About!!</h1>
  <router-link to="/">Go to home</router-link>
  <p>数字</p>
  <span>{{ val }}</span>
</template>

<script lang="ts">
  import { defineComponent, ref } from "vue";

  export default defineComponent({
    setup: () => {

      const val = ref(0);
      return { val };
    },
  });
</script>