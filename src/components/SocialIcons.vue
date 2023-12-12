
<template>
    <div class="social-icons">
      <a v-for="icon in icons" :key="icon.id" :href="`#${icon.name.toLowerCase()}`">
        <i :class="`fab fa-${icon.name.toLowerCase()}`"></i>
      </a>
    </div>
  </template>
  
  <script setup>
  const props = defineProps(['icons']);
  </script>
  
  <style scoped>
  .social-icons {
    display: flex;
    
  }
  
  .social-icons a {
    font-size: x-large;
    margin-right: 10px;
    color: rgb(83, 83, 83);
  }
  </style>
  
 
  <script>
  import '@fortawesome/fontawesome-free/css/all.css'; 
  </script>
  