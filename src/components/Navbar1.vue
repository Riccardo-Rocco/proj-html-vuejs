<template>
  <!-- Barra di navigazione -->
  <nav class="navbar">
      <!-- Contenitore per icone sociali -->
      <div class="social-icons">
          <!-- Componente SocialIcons per visualizzare icone sociali -->
          <SocialIcons :icons="socialIcons" />
      </div>
      <!-- Contenitore per testi alternativi -->
      <div class="alternate-text">
          <!-- Componente AlternateText per visualizzare testi alternativi -->
          <AlternateText :texts="alternateTexts" />
      </div>
      <!-- Contenitore per la barra di ricerca -->
      <div class="search">
          <!-- Componente Search per la barra di ricerca -->
          <Search />
      </div>
  </nav>
</template>

<script setup>
  // Importazione dei componenti necessari
  import SocialIcons from './SocialIcons.vue';
  import AlternateText from './AlternateText.vue';
  import Search from './SearchBar.vue';

  // Definizione delle proprietà (props)
  const props = defineProps(['socialIcons', 'alternateTexts']);
</script>

<style scoped>
  /* Stili CSS specifici per la barra di navigazione */
  .navbar {
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding-right: 10%;
      padding-left: 10%;
      background-color: #fffefe;
      color: rgb(0, 0, 0);
  }

  /* Margini per i contenitori interni */
  .social-icons,
  .alternate-text,
  .search {
      margin: 0;
  }
</style>
