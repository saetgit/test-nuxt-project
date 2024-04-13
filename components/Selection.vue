<template>
    <div>
      <multi-select v-model="selectedOptions" :options="options" />
    </div>
  </template>
  
  <script setup>
  import { ref } from 'vue';
  
  const selectedOptions = ref([]);
  const options = ref([
    { label: 'Option 1', value: 'option1' },
    { label: 'Option 2', value: 'option2' },
    { label: 'Option 3', value: 'option3' },
    { label: 'Option 4', value: 'option4' },
  ]);
  
  </script>
  