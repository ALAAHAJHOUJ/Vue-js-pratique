<script setup>

  /*import { ref } from 'vue'
  import Fichier from './Fichier.vue'
  import Fichier2 from './Fichier2.vue'

  const tableau=ref([1,2])
  const ref2=ref("")

  function sayHello(name) {
     tableau.value.push(tableau[tableau.length-1]+1)
  }

  function tester(valeur){
     ref2.value+=valeur
     console.log(ref2.value)
  }*/


 import { ref } from 'vue'
 import tester from './Tester.vue'
 let Aux=[]

 function chercher(valeur,nom){
    for(let i=0;i<Aux.length;i++){
       if(nom==Aux[i].nom){
           return Aux[i].nb++
       }
    }

    Aux.push({nom:nom,nb:valeur})
 }


 function Afficher(valeur,nom){
     chercher(valeur,nom)
     console.log(Aux)
 }




 

</script>



<template>
     <tester :value1="'boutayna'" :callback="Afficher"></tester>
     <tester :value1="'nouhaila'" :callback="Afficher"></tester>
     <tester :value1="'soukaina'" :callback="Afficher"></tester>
</template>



<style scoped>
  .class11{
   border: 1px solid black;
   width: 200px;
   height: 200px;
   display: flex;
   justify-content: center;
   align-items: center;
   cursor: pointer;
   margin-bottom: 20px;
  }
</style>
