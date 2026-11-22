<script setup>
import { onUpdated, ref } from "vue";

const props=defineProps(["valeur11"])


const tableau=ref([])


const Afficher1=ref(false)

const Envoyer=async()=>{
   try {
      const resultat1=await fetch("http://localhost:4000/tester11/")

      const resultat2=resultat1.headers.get("content-type")

      if(resultat2.includes("json")){
           const data=await resultat1.json();
           console.log(data)
           tableau.value=data
      }else {
           const data=await resultat1.text()

           console.log(data)
      }
   } catch (error) {
      console.log(error)
   }
}


</script>



<template>
    <div @click="Envoyer" class="class1">
       
       <div v-for="item in tableau" :key="item"  >
          {{"username:"+item.username}}
       </div>
    </div>
</template>


<style scoped>
 .class1{
    border: 1px solid black;
    width: 300px;
    height: 300px;
    display: flex ;
    justify-content: center;
    align-items: center;
 }
</style>