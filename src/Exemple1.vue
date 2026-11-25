<script setup>
import { onMounted } from "vue";

const socket=io("http://localhost:4000")


const Envoyer=()=>{

 socket.emit("message",document.getElementById("me112").value)

}

const Envoyer1=()=>{
   console.log("hey1")
   socket.emit("message","typing...")
}

const Envoyer2=()=>{
   console.log("hey2")
   socket.emit("message",{
      value:"",
      status:"finis"
   })
}


onMounted(()=>{
   socket.on("connection")

   socket.on("message",(data)=>{
      console.log(data)
      document.getElementById("me11").innerText=data
   })
})


</script>




<template>
    <div id="me11">

    </div>
   <div  class="border border-black w-[300px] h-[300px] flex flex-wrap justify-center  items-center box-border p-6 ">
        <input @focus="Envoyer1" @blur="Envoyer2" id="me112" placeholder="entrer une valeur" class="border border-black w-[190px] h-[40px] rounded-[10px] pl-3 box-border">
        <button  @click="Envoyer"  class="text-white p-6 bg-blue-500 hover:bg-blue-200 cursor-pointer rounded-[10px]">Envoi</button>
   </div>
</template>


<style scoped>

</style>