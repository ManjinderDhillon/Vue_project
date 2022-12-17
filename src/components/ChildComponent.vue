<template>
   
    <ul>
     <h2>Name: {{name}}{{fav   ? '(favorite)' : ''}}</h2>
     <button @click="toggleDetails" > {{ detailsAreVisible ? "Hide" : "Show" }}Details</button>
     <button @click="toggleFav" >toggleFavorite</button>
     <ul v-if="detailsAreVisible" >
       <li>
         <strong>Phone: {{phone}}</strong>
       </li>
       <li>
         <strong>Email: {{email}}</strong>
       </li>
     </ul>
    </ul>
    <button @click="emit('delete',id)" >Delete</button>
   
 </template>
 
 <script setup>
 
 import { ref , computed} from 'vue';
 const emit = defineEmits(['toggleFavorite','delete'])
 const props = defineProps({
  id:{type:String,required:false},
  name:{type:String,required:true},
  phone:{type:String,required:true},
  email:{type:String,required:true},
  favorite :{type:Boolean,required:false}

})
 const detailsAreVisible = ref(false);
 const fav =  ref(props.favorite)


 


const toggleFav=()=> {
emit('toggleFavorite',props.id)
 
}
 const toggleDetails = () => {
   detailsAreVisible.value = !detailsAreVisible.value;
 };

 </script>