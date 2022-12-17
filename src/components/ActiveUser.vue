<template>
<h1>Name: {{name}}</h1>
<h3>Age: {{age}}</h3>

</template>

<script setup >

const props = defineProps({
  name:{type:String},
  age:{type:Number}
  
})


</script>