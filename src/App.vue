<template>
  <div id="app">
    <Header />
    <Carousel />
    <ProductDisplay />
    <Collection />
    
    


    
  </div>
</template>

<script>
import Header from './components/Header.vue';
import Carousel from './components/Carousel.vue';
import ProductDisplay from './components/ProductDisplay.vue';
import Collection from './components/Collection.vue';


export default {
  components: {
    Header,
    Carousel,
    ProductDisplay,
    Collection,
  },
};
</script>

<style>

</style>
