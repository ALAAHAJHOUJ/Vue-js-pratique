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


   import tester3 from './Tester3.vue'

   const Aux=[1,2,3,4]
</script>



<template>
 
 <tester3 v-for="(Item,Index) in Aux" :key="Index" :cle1="Index" :longeur="Aux.length"></tester3>

</template>



<style scoped>
  .class11{
     text-align: center;
  }


  #mee1{
      background:gray;
      width:400px;
      height: 90px;
      display: flex;
      justify-content: center;
      gap: 20px;
      align-items: center;
      border-radius: 10px;
  }
</style>
