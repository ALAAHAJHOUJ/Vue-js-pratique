<script setup>
import { ref } from "vue";
const props=defineProps(["cle1","longeur"])

</script>


<template>
   <div id="me1" :class="props.cle1!=longeur-1?'class1':''">
       {{props.cle1}}
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