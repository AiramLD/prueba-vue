<template>
  <li>
    <span>{{ task.id }} : {{ task.name }}</span>
    <button @click="$emit('remove-task', task.id)">X</button>
  </li>
  <div>
    
  </div>
</template>
<script setup>
defineProps(['task']);
defineEmits(['remove-task']);
</script>
<style>
  
</style>