<script setup>
import CardComponent from '@/components/CardComponent.vue';

const users = [ 
   {
      name : 'juana de arcos',
      mail : 'juana@gmail.com',
   },

   {
      name : 'pablo de arcos',
      mail : 'pablo@gmail.com',
   }
]

</script>

<template>
 
<h1> 
   hola mundo
</h1>

<CardComponent v-for="(user,index) in users"  :key="index" :name="user.name" :mail ="user.mail"/>



</template>

<style >


</style>
