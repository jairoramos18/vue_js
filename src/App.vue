<script setup>
import CardComponent from '@/components/cardComponent.vue';

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

<CardComponent  v-for="user int users"  :key="usuario"/>


</template>

<style >


</style>
