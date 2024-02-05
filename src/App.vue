<template lang="">
  <h1>Lista de tareas</h1>
  <p>Se han encontrado {{tasks.length}} tareas</p>
  <p>{{textoNumeroTareas}}</p>
  <ul>
    <li v-for="task of tasks" :key="task.id">{{task.id}} - {{task.name}}</li>
  </ul>
</template>
<script setup>
import { computed, ref } from 'vue';
const tasks = ref([
  {id: 1, name: 'Corregir examen'},
  {id: 2, name: 'Leer'},
  {id: 3, name: 'Jugar'},
  {id: 4, name: 'Dormir'}
]);

const textoNumeroTareas = computed(()=>{
  // if(tasks.value.length == 0){
  //   return 'No hay tareas';
  // }else if(tasks.value.length == 1){
  //   return 'Hay una tarea';
  // }else{
  //   return 'Hay ' + tasks.value.length + ' tareas';
  // }
  if(tasks.value.length == 0) return 'No hay tareas';
  else if(tasks.value.length == 1) return 'Hay una tarea';
  return 'Hay ' + tasks.value.length + ' tareas';
});
</script>
<style lang="">
  
</style>