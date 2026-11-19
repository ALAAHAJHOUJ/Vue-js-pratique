<script setup>
  import { ref } from "vue"


  const props=defineProps(["value1","callback"])



  const ref1=ref(0)

  function Afficher(){
       props.callback(ref1.value,props.value1)
  }

  
  const changer=()=>{
     ref1.value++
     Afficher()
  }
 
</script>



<template>
     <div @click="changer"  style="width:200px;height:200px;border:1px solid black;display:flex;justify-content:center;align-items:center;margin-top:20px">
            {{ref1}}
     </div>
</template>



<style scoped>

</style>