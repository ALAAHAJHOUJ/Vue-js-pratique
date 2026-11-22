<script setup>
  import { onUnmounted, ref } from "vue"


  const props=defineProps(["value1","callback","Longeur","Index","Supp"])



  const ref1=ref(0)

  
  const changer=()=>{
     ref1.value++
     Afficher()
  }

  const Supp2=()=>{
       props.Supp(props.value1)
  }

</script>



<template>
     <div @click="callback" @mouseleave="Supp2" :class="{ 'active': props.Longeur-1==props.Index }" style="width:200px;height:200px;border:1px solid black;display:flex;justify-content:center;align-items:center;margin-top:20px">
            {{value1}}
     </div>
</template>



<style scoped>

.active{
    margin-bottom: 40px;
}
</style>