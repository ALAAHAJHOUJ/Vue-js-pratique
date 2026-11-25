<script setup>
import { onUpdated, ref } from "vue";
const props=defineProps(["cle1","longeur","valeur2","callback"])

const Ajouter=()=>{
    fetch("http://localhost:4000/Ajouter12/",{method:"POST",body:JSON.stringify({valeur11:props.cle1}),headers:{"Content-Type": "application/json",}})
    .then((res)=>{console.log(res);return res.text()})
    .then((res)=>{console.log(res)})
    .catch((err)=>{console.log(err)})
}
</script>


<template>
   <div @click="Ajouter"  id="me1" :class="props.cle1!=longeur-1?'class1':''">
       {{props.valeur2==true?"HEY":"HEY22"}}
   </div>

  
</template>


<style scoped>

#me1{
    border: 1px solid black;
    width: 300px;
    height: 300px;
    display: flex;
    justify-content: center;
    align-items: center;
}

.class1{
    margin-top: 40px;
}
</style>