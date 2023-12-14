<template>
  <!-- Contenitore per il testo alternativo corrente -->
  <div class="alternate-text">
      {{ currentAlternateText }}
  </div>
</template>

<script setup>
  // Importazione delle funzioni necessarie da Vue
  import { ref, onMounted, onBeforeUnmount, defineProps, computed } from 'vue';

  // Definizione delle proprietà (props)
  const props = defineProps(['texts']);

  // Variabile reattiva per indicizzare il testo alternativo corrente
  const currentAlternateTextIndex = ref(0);

  // Identificativo dell'intervallo per l'aggiornamento automatico del testo
  let intervalId;

  // Funzione per aggiornare il testo alternativo
  const updateAlternateText = () => {
      currentAlternateTextIndex.value = (currentAlternateTextIndex.value + 1) % props.texts.length;
  };

  // Gestione del ciclo di vita del componente
  onMounted(() => {
      intervalId = setInterval(updateAlternateText, 5000);
  });

  onBeforeUnmount(() => {
      clearInterval(intervalId);
  });

  // Proprietà calcolata per ottenere il testo alternativo corrente
  const currentAlternateText = computed(() => props.texts[currentAlternateTextIndex.value]);
</script>

<style scoped>
  /* Stili CSS specifici per il testo alternativo */
  .alternate-text {
      font-size: 18px;
      font-weight: bold;
      color: rgb(73, 111, 201);
  }
</style>
