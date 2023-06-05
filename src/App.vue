<script setup>
import CardComponent from '@/components/CardComponent.vue';
import {  ref } from 'vue';
const borrarTarjeta = (index) =>{
   console.log('kill to', index)
users.value.splice(index , 1)
console.log(users)
}
const users = ref([ 
   {
      name : 'juana de arcos',
      mail : 'juana@gmail.com',
   },

   {
      name : 'pablo de arcos',
      mail : 'pablo@gmail.com',
   }
])

</script>

<template>
 
<h1> 
   hola mundo
</h1>
<input type="text" v-model="name" placeholder="escriba tu nombre " class=" border rounded"><br><br>
<input type="text" v-model="mail" placeholder="escriba su correo " class=" border rounded"><br><br>
<button class=""></button>


<div class=" space-y-8">
   <CardComponent v-for="(user,index) in users"  :key="index" :name="user.name" :mail ="user.mail"  @borrarTarjeta = "borrarTarjeta"/>

</div>





</template>

<style >


</style>
