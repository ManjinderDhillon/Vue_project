<template>
 <SlotTwo>
    <template v-slot:header >
        <h2>Slots</h2>
    </template>
  </SlotTwo>

  <SlotTwo>
    <template #default="slotsProp">
      <h2>{{ slotsProp.item }}</h2>
    </template>
  </SlotTwo>
 
</template>

<script setup>
import SlotTwo from "./SlotTwo.vue";
</script>
