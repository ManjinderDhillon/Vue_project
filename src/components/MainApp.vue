<template>
   <ActiveUser  :name="name" :age="age"/>
   <UserData @addData="newContact" />
</template>

<script setup>
import ActiveUser from "./ActiveUser.vue";
import UserData from './UserData.vue';
import { ref } from "vue";
const name = ref('RamlSingh')
const age = ref(25)

const newContact = (Nname,Nage)=> {
name.value = Nname.value
age.value = Nage.value
}

</script>
