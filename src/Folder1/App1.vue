<script setup>0
import { ref } from "vue";


const nbFois=ref(0)
const finis=ref(false)
function Afficher(){

    if(finis.value) return 
    if(nbFois.value>=3) {finis.value=true;return console.log("vous avez atteint le nombre maximium d'essaye")}


    class User{
         constructor(username,password){
             this.username=username;
             this.password=password;
         }


    }

    const user1=new User("hajhouj","2001HAJHOUJ$$$")
    console.log(user1)
    nbFois.value++
}

</script>


<template>
   <div @click="Afficher" class="border border-black flex justify-center items-center w-[300px] h-[300px]">

   </div>
</template>


<style scoped>

</style>