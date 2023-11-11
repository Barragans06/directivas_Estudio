<script setup>

import { ref } from 'vue';

let newTaks = ref ('')
let listTasks = ref ([
  {
  name : 'Comer' ,
  done : true},
  {
    name : 'Ejercicio' ,
    done : false},
  {
    name : 'Dormir' , 
    done : false}
  
])

</script>

<template>
  <div class="container">
    <div>
      <h1>Welcome to my list</h1>
      <p class="subtitle">{{ newTaks }}</p>
      <div>
        <div class="taks"> {{ listTasks.name }} <span class="bton">one</span></div>
       
      </div>
      <div>
        <input v-model="newTaks" type="text" placeholder="Escriba su tarea">
        <p v-show="newTaks != '' " > Presione "enter" para enviar</p>
      </div>
    </div>
  </div>
</template>

<style scoped>


.container{
  font-family: 'Hanken Grotesk', sans-serif;
  font-family: 'Montserrat', sans-serif;
  margin: 0 auto;
  text-align: center;
  align-items: center;
  background-color: #6ACFC9;
  width: 420px;
  border-radius: 10px;
  padding: 6px 12px;
  
  
}
.taks{
  display: flex;
  justify-content: space-between;
  background-color: #AEE8CA;
  border-radius: 3px;
  margin-bottom: 2px; 
  padding: 5px 5px 5px 5px;
}
.bton{
  background-color: #3C2F80;
  display: inline-block;
  padding: 0 6px;
  border-radius: 3px; 
  justify-content: space-evenly;
  color: white;
}
.bton:hover{
cursor: pointer;
background-color: #26B6C6;
opacity: 0.4;
}
input{
  
  border: none;
  border-radius: 3px;
  padding: 2px 6px;
   width: 100%;
   box-sizing: border-box;
   margin-top: 12px;
   padding: 7px 7px 7px 7px;
   background-color: #AEE8CA;

}


</style>
