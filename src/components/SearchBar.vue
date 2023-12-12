
<template>
    <div class="search">
      <input type="text" v-model="searchText" placeholder="Cerca..." @input="emitSearchChange" />
    </div>
  </template>
  
  <script setup>
  import { ref, defineProps, defineEmits } from 'vue';
  
  const props = defineProps(['searchText']);
  const { emit } = defineEmits();
  
  const emitSearchChange = () => {
    emit('search-change', searchText);
  };
  
  const searchText = ref(props.searchText);
  </script>
  
  <style scoped>
  .search {
    display: flex;
    align-items: center;
  }
  
  .search input {
    padding: 5px;
    margin-left: 5px;
  }
  </style>
  