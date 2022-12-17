<template>
<form @submit.prevent="addFriend" >
    <div>
        <label >Name: </label>
        <input type="text" v-model="Name"  >
    </div>
    <div>
        <label  >Phone: </label>
        <input type="text" v-model="Phone" >
    </div>
    <div>
        <label  >Email: </label>
        <input type="text" v-model="Email">
    </div>
    <div>
        <button @click="addFriend" >Add Contact</button>
    </div>
    
</form>
</template>

<script setup >
import { ref } from 'vue';
const emit = defineEmits(['addContact'])


const Name = ref('');
const Phone = ref('');
const Email = ref('');

const addFriend = () => {
    emit('addContact',Name,Phone,Email)
}

</script>