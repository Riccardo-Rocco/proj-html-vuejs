
<template>
    <nav class="navbar">
      <div class="social-icons">
        <SocialIcons :icons="socialIcons" />
      </div>
      <div class="alternate-text">
        <AlternateText :texts="alternateTexts" />
      </div>
      <div class="search">
        <Search />
      </div>
    </nav>
  </template>
  
  <script setup>
  import SocialIcons from './SocialIcons.vue';
  import AlternateText from './AlternateText.vue';
  import Search from './SearchBar.vue';
  
  const props = defineProps(['socialIcons', 'alternateTexts']);
  </script>
  
  <style scoped>
  .navbar {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding-right: 10%;
    padding-left: 10%;
    background-color: #fffefe;
    color: rgb(0, 0, 0);
    
  }
  
  .social-icons,
  .alternate-text,
  .search {
    margin: 0;
  }
  </style>
  