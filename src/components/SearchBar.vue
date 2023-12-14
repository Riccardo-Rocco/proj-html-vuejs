<template>
  <!-- Componente di ricerca con un campo di testo -->
  <div class="search">
      <input type="text" v-model="searchText" placeholder="Cerca..." @input="emitSearchChange" />
  </div>
</template>

<script setup>
  // Importazione delle funzioni necessarie da Vue
  import { ref, defineProps, defineEmits } from 'vue';

  // Definizione delle proprietà (props) e degli eventi (emits) per il componente
  const props = defineProps(['searchText']);
  const { emit } = defineEmits();

  // Funzione per emettere un evento di cambio di ricerca
  const emitSearchChange = () => {
      emit('search-change', searchText);
  };

  // Variabile reattiva per memorizzare il testo di ricerca
  const searchText = ref(props.searchText);
</script>

<style scoped>
  /* Stile per il componente di ricerca */
  .search {
      display: flex;
      align-items: center;
  }

  .search input {
      padding: 5px;
      margin-left: 5px;
  }
</style>
