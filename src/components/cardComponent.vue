<script  setup >
const mensaje =  () => {
 console.log("mensaje");
}
const borrarTarjeta = (index) => {
console.log('Borrar tarjeta',index);
emit('borrarTarjeta' , index)
 
}
const emit = defineEmits(['borrarTarjeta'])
const props = defineProps({
    name : {
        type : String,
        default : 'no name'
    },
    mail :{
        type : String,
        default : 'no mail'
    },
    
        index : {
            type : Number
        } 
    
})

</script>

<template>
    <div class="w-48 rounded shadow overflow-hidden">
   <div class=" inline-block  align-top ">
      <img src="https://img.freepik.com/foto-gratis/disparo-gran-angular-solo-arbol-que-crece-cielo-nublado-puesta-sol-rodeada-cesped_181624-22807.jpg" alt="">
   </div>
   <div class=" inline-block">
      <h2 class="text-md font-semibold"> {{ props.name }} </h2>
      <p class=" text-xs leading-0 "> {{ props.mail }}</p>
      <span class=" inline-block ml-4 bg-red-600  text-white rounded leading-0  py-0 px-2 m-2 hover:cursor-pointer hover:bg-red-700   " @click="Sevent =>borrarTarjeta(props,index)">
        x
      </span>
   </div>
</div>

</template>