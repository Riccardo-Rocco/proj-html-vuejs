<template>
    <div class="Title-Container">
      <h1>Best Seller</h1>
      <h4>Must-have products from our top sellers</h4>
    </div>
  
    <swiper
      ref="{swiperRef}"
      :slidesPerView="5"
      :centeredSlides="true"
      :pagination="{ type: 'fraction' }"
      :navigation="true"
      :loop="true"
      :modules="modules"
      class="mySwiper"
    >
      <swiper-slide>
        <div class="card">
          <img src="../assets/images/black_elegant_leather_jacket-200x260.jpg" alt="">
          <div class="card-overlay">
            <h5>Black Elegant Leather Jacket</h5>
            <p>Men, Jackets, Jeans</p>
            <p>$200</p>
          </div>
        </div>
      </swiper-slide>
      <swiper-slide>
        <div class="card">
          <img src="../assets/images/black_leather_jacket-200x260.jpg" alt="">
          <div class="card-overlay">
            <h5>Black Leather Jacket</h5>
            <p>Jackets, Men</p>
            <p>$176</p>
          </div>
        </div>
      </swiper-slide>
      <swiper-slide>
        <div class="card">
          <img src="../assets/images/blue_jacket_and_white_stripe_tee-200x260.jpg" alt="">
          <div class="card-overlay">
            <h5>Blue Jacket & Stripe Tee</h5>
            <p>Jackets, Men, Suits</p>
            <p>$580</p>
          </div>
        </div>
      </swiper-slide>
      <swiper-slide>
        <div class="card">
          <img src="../assets/images/blue_leather_jacket-200x260.jpg" alt="">
          <div class="card-overlay">
            <h5>Modern Black Leather Suit</h5>
            <p>Jackets, Men</p>
            <p>$96</p>
          </div>
        </div>
      </swiper-slide>
      <swiper-slide>
        <div class="card">
          <img src="../assets/images/spring_printed_dress-200x260.jpg" alt="">
          <div class="card-overlay">
            <h5>Spring Printed Dress</h5>
            <p>Dress, Women</p>
            <p>$47</p>
          </div>
        </div>
      </swiper-slide>
      <swiper-slide>
        <div class="card">
          <img src="../assets/images/modern_love_tee-200x260.jpg" alt="">
          <div class="card-overlay">
            <h5>Modern Love Tee</h5>
            <p>T-Shirts, Women</p>
            <p>$68</p>
          </div>
        </div>
      </swiper-slide>
      <swiper-slide>
        <div class="card">
          <img src="../assets/images/black_leather_suit-200x260.jpg" alt="">
          <div class="card-overlay">
            <h5>Black Leather Suit</h5>
            <p>Jackets, Men</p>
            <p>$176</p>
          </div>
        </div>
      </swiper-slide>
      <swiper-slide>
        <div class="card">
          <img src="../assets/images/hipster_black_top-200x260.jpg" alt="">
          <div class="card-overlay">
            <h5>Hipster Black Top</h5>
            <p>T-Shirts, Women</p>
            <p>$57</p>
          </div>
        </div>
      </swiper-slide>
    </swiper>
  
    <p class="append-buttons"></p>
  </template>
  
  <script>
  import { Swiper, SwiperSlide } from 'swiper/vue';
  import 'swiper/css';
  import 'swiper/css/pagination';
  import 'swiper/css/navigation';
  import { Pagination, Navigation } from 'swiper/modules';
  
  export default {
    components: {
      Swiper,
      SwiperSlide,
    },
    setup() {
      return {
        modules: [Pagination, Navigation],
      };
    },
  };
  </script>
  
  <style scoped>
  .Title-Container {
    margin-top: 30px;
    margin-bottom: 50px;
    text-align: center;
  }
  
  .swiper {
    width: 75%;
  }
  
  .swiper-slide {
    position: relative;
    
  }
  
  .swiper-slide img {
    width: 100%;
    height: auto;
    transition: transform 0.3s ease-in-out;
    
  }
  
 
   
  .card{
    border: none;
  }
  .card-overlay {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-color: rgba(255, 165, 0, 0.7);
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    opacity: 0;
    transition: opacity 0.3s ease-in-out;
   
  }
  
  .swiper-slide:hover .card-overlay {
    opacity: 1;
  }
  

  .card-overlay h5,
  .card-overlay p {
    color: #fff; 
    margin: 2px;
  }
  </style>