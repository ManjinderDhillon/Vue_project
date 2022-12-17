<template>
  <ChildComponent
    v-for="friend in friends"
    :key="friend.index"
    :id="friend.id"
    :name="friend.name"
    :phone="friend.phone "
    :email="friend.email "
    :favorite="true"
    @toggleFavorite="toggle"
  />
</template>
<script setup>
import { ref } from "vue";
import ChildComponent from "./ChildComponent.vue";

const friends = ref([
  {
    id: "Aman",
    name: "AmanPreet",
    phone: "5566778800",
    email: "Aman@gmail.com",
    favorite: true,
  },
  {
    id: "Raman",
    name: "ramanPreet",
    phone: "677885500",
    email: "Rman@gmail.com",
    favorite: true,
  },
]);
const toggle = (friendId) => {
    alert(friendId) 
};
</script>
