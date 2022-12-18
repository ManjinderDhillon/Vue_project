<template>
<SlotTwo>
    <template v-slot:header >
        <h1>Slots Info</h1>
    </template>
    <template v-slot:info >
<p>Slots Are the Advanced part of VueJs</p>
    </template>
    <template v-slot:btn >
        <button>Submit</button>
    </template>
</SlotTwo>
</template>

<script setup >
import SlotTwo from './SlotTwo.vue';

</script>