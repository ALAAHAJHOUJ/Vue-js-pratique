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


 import { onMounted,onUpdated, ref } from 'vue'
 import tester from './Tester.vue'



function tester77(){
   class Exemple{
       constructor(id,name){
          this.id=id;
          this.name=name;
       }
   }

   const Aux=[]
   for(let i=0;i<10;i++){
      Aux.push(new Exemple(i+1,`Exemple${i+1}`))
   }

   console.log(Aux)
}

onUpdated(()=>{
    tester77()
})

const ref1=ref(0)
function Changer(){
    ref1.value++
}

</script>



<template>
     <!--tester :value1="'boutayna'" :callback="Afficher"></tester>
     <tester :value1="'nouhaila'" :callback="Afficher"></tester>
     <tester :value1="'soukaina'" :callback="Afficher"></tester-->

     <div @click="Changer" class="class11">
       click {{ref1}}
     </div>

     <tester v-if="ref1%2==0"></tester>
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
