<template>
    <div class="Title-Container">
      <h1>New Arrivals</h1>
      <h4>Brand new products from top designers</h4>
    </div>
  
    <swiper
      ref="{swiperRef}"
      :slidesPerView="5"
      :centeredSlides="true"
      :pagination="{ type: 'fraction' }"
      :navigation="true"
      :loop="true"
      :autoplay="{ delay: 3000, disableOnInteraction: false }"
      :modules="modules"
      class="mySwiper"
    >
      <swiper-slide>
        <div class="card">
          <img src="../assets/images/black_elegant_leather_jacket-400x520.jpg" alt="">
          <div class="card-overlay">
            <h5>Black Elegant Leather Jacket</h5>
            <p>Men, Jackets, Jeans</p>
            <p class="original-price" >$235</p>
            <p>$200</p>
          </div>
        </div>
      </swiper-slide>
      <swiper-slide>
        <div class="card">
          <img src="../assets/images/black_leather_jacket-400x520.jpg" alt="">
          <div class="card-overlay">
            <h5>Black Leather Jacket</h5>
            <p>Jackets, Men</p>
            <p>$176</p>
          </div>
        </div>
      </swiper-slide>
      <swiper-slide>
        <div class="card">
          <img src="../assets/images/blue_jacket_and_white_stripe_tee-400x520.jpg" alt="">
          <div class="card-overlay">
            <h5>Blue Jacket & Stripe Tee</h5>
            <p>Jackets, Men, Suits</p>
            <p>$580</p>
          </div>
        </div>
      </swiper-slide>
      <swiper-slide>
        <div class="card">
          <img src="../assets/images/blue_leather_jacket-400x520.jpg" alt="">
          <div class="card-overlay">
            <h5>Modern Black Leather Suit</h5>
            <p>Jackets, Men</p>
            <p>$96</p>
          </div>
        </div>
      </swiper-slide>
      <swiper-slide>
        <div class="card">
          <img src="../assets/images/spring_printed_dress-400x520.jpg" alt="">
          <div class="card-overlay">
            <h5>Spring Printed Dress</h5>
            <p>Dress, Women</p>
            <p>$47</p>
          </div>
        </div>
      </swiper-slide>
      <swiper-slide>
        <div class="card">
          <img src="../assets/images/modern_love_tee-400x520.jpg" alt="">
          <div class="card-overlay">
            <h5>Modern Love Tee</h5>
            <p>T-Shirts, Women</p>
            <p>$68</p>
          </div>
        </div>
      </swiper-slide>
      <swiper-slide>
        <div class="card">
          <img src="../assets/images/black_leather_suit-400x520.jpg" alt="">
          <div class="card-overlay">
            <h5>Black Leather Suit</h5>
            <p>Jackets, Men</p>
            <p>$176</p>
          </div>
        </div>
      </swiper-slide>
      <swiper-slide>
        <div class="card">
          <img src="../assets/images/hipster_black_top-400x520.jpg" alt="">
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
  import 'swiper/css/navigation';
  import 'swiper/css/pagination';
  import 'swiper/css/navigation';
  import { Pagination, Navigation, Autoplay } from 'swiper/modules';
  
  export default {
    components: {
      Swiper,
      SwiperSlide,
    },
    setup() {
      return {
        modules: [Pagination, Navigation, Autoplay],
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

  .original-price {
    text-decoration: line-through;
    margin-right: 0.5rem; 
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
    background: linear-gradient(180.3deg, rgb(214, 224, 255) 20.2%, rgb(254, 168, 168) 100.3%);
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