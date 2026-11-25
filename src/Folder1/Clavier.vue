<script setup>
import { ref } from "vue";

const tableau=ref([])


function Remplir(){
    for (let i = 65; i <= 90; i++) {
        tableau.value.push(String.fromCharCode(i));
    }
}

Remplir()

let Aux1=""
function Afficher(valeur){      
   if(Aux1.length==12) return 
   if(valeur.trim()!="")
     document.getElementById("mee11").innerHTML+=valeur
   else 
    document.getElementById("mee11").innerHTML+="&nbsp;" 

   Aux1+="h"
}


function Supprimer(){
     Aux1=Aux1.slice(0,-1)
     document.getElementById("mee11").innerText=document.getElementById("mee11").innerText.slice(0,-1)
}
</script>



<template>
   <button @click="Supprimer" class="bg-red-500 text-white rounded-[10px] p-3.5 hover:bg-red-200">
      Supprimer
   </button>
   <div  class="border-black border-[1px] flex flex-wrap justify-center items-center gap-3 w-[400px] h-[600px]">
       <div  v-for="item in tableau" :key="item" @click="()=>{Afficher(item)}" class="bg-blue-500 hover:bg-blue-300 text-white w-[50px] h-[50px] flex justify-center items-center rounded-[10px]">
          {{item}}
       </div>

       <div class="w-full h-[60px] flex justify-center items-center">
         <div  class="bg-blue-500 hover:bg-blue-300 rounded-[10px] h-[50px] w-[160px]" @click="()=>{Afficher(' ')}">

         </div>
       </div>
   </div>

   <div id="mee11" class="text-center w-[130px] h-[50px] ">

   </div>
</template>




<style scoped>

</style>