
<template>
    <header>
      <Navbar1 :socialIcons="socialIcons" :alternateTexts="alternateTexts" />
      <NavBar2 />
    </header>
  </template>
  
  <script setup>
  import Navbar1 from './Navbar1.vue';
  import NavBar2 from './NavBar2.vue';
  
  const socialIcons = [
    { id: 1, name: 'Facebook' },
    { id: 2, name: 'Twitter' },
    { id: 3, name: 'Instagram' },
    { id: 4, name: 'Youtube' },
    { id: 5, name: 'Pinterest' }
  ];
  
  const alternateTexts = [
    '15% OFF YOUR FIRST ORDER!',
    'FREE STANDARD SHIPPING ON ORDERS OVER $49'
  ];
  </script>
  
  <style>
  header {
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    background-color: white;
    padding: 10px;
    margin-bottom: 2%;

    
  }
  </style>
  