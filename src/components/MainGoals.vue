<template>
  <button @click="setGoals('ActiveGoals')">Active Goals</button>
  <button @click="setGoals('ManageGoals')">Manage Goals</button>
  <!-- <ActiveGoals v-if="selectedComponent === 'ActiveGoals'" />
  <ManageGoals v-if="selectedComponent === 'ManageGoals' "/>  -->
  <KeepAlive>
    <component :is="selectedComponent" />
  </KeepAlive>
</template>

<script setup>
import { ref } from "vue";
import ActiveGoals from "./ActiveGoals.vue";
import ManageGoals from "./ManageGoals.vue";
const selectedComponent = ref("ActiveGoals");
const setGoals = (cmp) => {
  selectedComponent.value = cmp;
};
</script>
