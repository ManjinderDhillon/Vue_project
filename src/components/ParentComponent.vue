<template>
  <NewFriend @addContact="addNewFriend" />
  <ChildComponent
    v-for="friend in friends"
    :key="friend.id"
    :id="friend.id"
    :name="friend.name"
    :phone="friend.phone "
    :email="friend.email "
    :favorite="true"
    @toggleFavorite="toggle"
    @delete="deleteContact"
  />
</template>
<script setup>
import { ref } from "vue";
import ChildComponent from "./ChildComponent.vue";
import NewFriend from './NewFriend.vue';

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
const addNewFriend = (Name,Phone,Email) => {
  const UserData = {
    id: '',
    name : Name,
    phone:Phone,
    email:Email,
    favorite:false
  }
  friends.value.push(UserData)
}
const deleteContact = (friendId) => {
 friends.value = friends.value.filter((friend)=>friend.id !== friendId)
}

</script>
