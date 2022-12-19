
<template>
  <slot name="header" ></slot>
  
    <p v-for="goal in goals" :key="goal.goal" >
      <slot :item="goal" ></slot>
    </p>
  
  
</template>

<script setup>
import { ref } from 'vue';
const goals = ref([
  'finish the course','learn Vue'
])
</script>
