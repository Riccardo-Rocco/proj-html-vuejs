<template>
  <!--primo carosello slid con swiper jumbotron sotto navbar -->
  <Swiper :navigation="true" :modules="modules" :autoplay="{ delay: 5000, disableOnInteraction: false }" loop class="mySwiper">
    <SwiperSlide>
      <img src="../assets/images/home1_slide_one_bg.jpg" alt="Image 1" class="d-block w-100">
      <div class="carousel-caption">
        <h1>Avada Classic Shop</h1>
        <h6>SHOW YOUR PRODUCTS WITH STYLE</h6>
        <button @click="handleButtonClick">GET AVADA NOW!</button>
      </div>
    </SwiperSlide>
    <SwiperSlide>
      <img src="../assets/images/home1_slide_2_bg.jpg" alt="Image 2" class="d-block w-100">
      <div class="carousel-caption">
        <h1>Online Store</h1>
        <h6>SELL YOUR PRODUCTS WITH STYLE</h6>
        <button @click="handleButtonClick">MEN</button>
        <button class="SpaceLeft" @click="handleButtonClick">WOMEN</button>
      </div>
    </SwiperSlide>
    <SwiperSlide>
      <img src="../assets/images/home1_slide_three_bg_2.jpg" alt="Image 3" class="d-block w-100">
      <div class="carousel-caption">
        <h1>Brand New Arrivals</h1>
        <h6>NEW COLLECTION FROM NEW YORK</h6>
        <button @click="handleButtonClick">VIEW ALL</button>
        <button class="SpaceLeft" @click="handleButtonClick">LOOKBOOK</button>
      </div>
    </SwiperSlide>
  </Swiper>
</template>

<script>
import { Swiper, SwiperSlide } from 'swiper/vue';
import 'swiper/css';
import 'swiper/css/navigation';


import { Navigation, Autoplay } from 'swiper/modules';

export default {
  components: {
    Swiper,
    SwiperSlide,
  },
  setup() {
    return {
      modules: [Navigation, Autoplay],
    };
  },
  methods: {
    handleButtonClick() {
      
      console.log('Hai cliccato su un pulsante dello slider');
    },
    
  },
};
</script>

<style scoped>
.carousel-caption {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  text-align: center;
  color: #fff; 
}

.carousel-caption h1 {
  font-size: 3.8em; 
}

.carousel-caption h6 {
  font-size: 1.8em; 
}

.carousel-caption button {
  padding: 10px 20px;
  font-size: 1em;
  background-color: transparent; 
  color: #fff; 
  border: solid 1px white;
  border-radius: 20px;
  cursor: pointer;
  
  
}

img{
  min-height: 600px;

  
  
}
.SpaceLeft{
  margin-left: 1rem;
}
</style>
