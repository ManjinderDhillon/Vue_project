<template>
  <form @submit.prevent="submitData" >
    <div><input type="text" placeholder="Name" v-model="name" /></div>
    <div><input type="number" placeholder="age" v-model="age" /></div>
    <button  >Set Data</button>
  </form>
</template>

<script setup>
import { ref } from "vue";
const emit = defineEmits(['addData'])
const name = ref("");
const age = ref("");
const submitData = () => {
    emit('addData',name,age)
};
</script>
