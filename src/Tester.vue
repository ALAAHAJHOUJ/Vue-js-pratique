<script setup>
  import { onUnmounted, ref } from "vue"


  const props=defineProps(["value1","callback"])



  const ref1=ref(0)

  
  const changer=()=>{
     ref1.value++
     Afficher()
  }

 
</script>



<template>
     <div  style="width:200px;height:200px;border:1px solid black;display:flex;justify-content:center;align-items:center;margin-top:20px">
            {{value1}}
     </div>
</template>



<style scoped>

</style>