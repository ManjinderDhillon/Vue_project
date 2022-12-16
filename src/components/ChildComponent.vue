<template>
   <li v-for="friend in friends" >
    <h2>Name: {{friend.name}}</h2>
    <button @click="toggleDetails" > {{ detailsAreVisible ? "Hide" : "Show" }}Details</button>
    <ul v-if="detailsAreVisible" >
      <li>
        <strong>Phone: {{friend.phone}}</strong>
      </li>
      <li>
        <strong>Email: {{friend.email}}</strong>
      </li>
    </ul>
  </li>
</template>

<script setup>
import { ref } from 'vue';

const detailsAreVisible = ref(false);

const friends = ref([
  {
    id: "Aman",
    name: "AmanPreet",
    phone: "5566778800",
    email: "Aman@gmail.com",
    isFavorite: true,
  },
  {
    id: "Raman",
    name: "RmanPreet",
    phone: "9988776655",
    email: "Rman@gmail.com",
    isFavorite: false,
  },
]);
console.log(friends);
const toggleDetails = () => {
  detailsAreVisible.value = !detailsAreVisible.value;
};
</script>
