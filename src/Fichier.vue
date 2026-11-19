<script setup>
import { ref } from "vue";

  const props = defineProps({
     fonction1:Function,
     nombre:Number,
     fonction:Function
  })

  const ref1=ref("hajhouj")
  const ref2=ref(0)

  const Ajouter=()=>{
    if(ref2.value==20) return 
    ref1.value+=" hajhouj"
    ref2.value++
  }


  function tester1(){
      props.fonction("hajhouj")
  }

  
</script>


<template>
    <div @click  id="mee">
         {{ref1}}
    </div>

    <div @click="tester1" style="margin-top:20px;text-align:center;height:50px">
      {{ref1=="hajhouj"?' Bonjour ! Le div est affiché.':''}}
     
    </div>
</template>




//le style de l'element 
<style scoped>
  #mee{
   width: 300px;
   height: 300px;
   border-radius: 10px;
   display: flex;
   justify-content: center;
   align-items: center;
   font-weight: bold;
   font-size: 20px;
   font-family: sans-serif;
   box-shadow: rgba(0, 0, 0, 0.35) 0px 5px 15px;
   text-align: center;
  }
</style>