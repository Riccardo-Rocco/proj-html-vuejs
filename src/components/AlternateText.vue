
<template>
    <div class="alternate-text">
      {{ currentAlternateText }}
    </div>
  </template>
  
  <script setup>
  import { ref, onMounted, onBeforeUnmount, defineProps, computed } from 'vue';
  
  const props = defineProps(['texts']);
  const currentAlternateTextIndex = ref(0);
  let intervalId;
  
  const updateAlternateText = () => {
    currentAlternateTextIndex.value = (currentAlternateTextIndex.value + 1) % props.texts.length;
  };
  
  onMounted(() => {
    intervalId = setInterval(updateAlternateText, 5000);
  });
  
  onBeforeUnmount(() => {
    clearInterval(intervalId);
  });
  
  const currentAlternateText = computed(() => props.texts[currentAlternateTextIndex.value]);
  </script>
  
  <style scoped>
  .alternate-text {
    font-size: 18px;
    font-weight: bold;
    color: rgb(73, 111, 201);
  }
  </style>
  