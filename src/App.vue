<template>
  <div id="app">
    <Header />
    <Carousel />
    <ProductDisplay />
    <Collection />
    <Carousel2 />
    
    


    
  </div>
</template>

<script>
import Header from './components/Header.vue';
import Carousel from './components/Carousel.vue';
import ProductDisplay from './components/ProductDisplay.vue';
import Collection from './components/Collection.vue';
import Carousel2 from './components/Carousel2.vue';


export default {
  components: {
    Header,
    Carousel,
    ProductDisplay,
    Collection,
    Carousel2,
},
};
</script>

<style>

</style>
