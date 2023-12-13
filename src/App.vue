<template>
  <div id="app">
    <Header />
    <Carousel />
    <ProductDisplay />
    <Collection />
    <Carousel2 />
    <Shipping />
    <Carousel3 />
    <Testimonial />
    <Blog />
    
    
    


    
  </div>
</template>

<script>
import Header from './components/Header.vue';
import Carousel from './components/Carousel.vue';
import ProductDisplay from './components/ProductDisplay.vue';
import Collection from './components/Collection.vue';
import Carousel2 from './components/Carousel2.vue';
import Shipping from './components/Shipping.vue';
import Carousel3 from './components/Carousel3.vue';
import Testimonial from './components/Testimonial.vue';
import Blog from './components/Blog.vue';


export default {
  components: {
    Header,
    Carousel,
    ProductDisplay,
    Collection,
    Carousel2,
    Shipping,
    Carousel3,
    Testimonial,
    Blog,

},
};
</script>

<style>

</style>
