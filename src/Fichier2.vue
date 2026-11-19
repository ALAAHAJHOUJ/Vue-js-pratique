<script setup>
import { ref } from "vue";
const ref1=ref(true)

function changer1(){
     ref1.value=!ref1.value
     console.log(ref1.value)
}
</script>




<template>
    <div @click="changer1" :class="ref1?'class1':'class2'" >
  
    </div>
</template>



<style scoped>
.class1{
 border: 1px solid black;
 width: 300px;
 height: 300px;
 border-radius: 10px;
}


.class2{
 border: 1px solid black;
 width: 300px;
 height: 300px;
}
</style>