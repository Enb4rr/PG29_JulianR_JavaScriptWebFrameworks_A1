<script setup lang="ts">
  import { useCounterStore } from "@/stores/counter.ts";
  const store = useCounterStore();
</script>

<template>
  <section class="counter">
    <h2>Counter:</h2>
    <p>Count: {{ store.count }}</p>
    <p>Double: {{ store.doubleCount }}</p>
    
    <button @click="store.increment">Increment</button>
  </section>
</template>

<style scoped>
  .counter {
    border: 1px solid #ccc;
    border-radius: 12px;
  }
  
  button {
    padding: 10px 10px;
    cursor: pointer;
  }
</style>