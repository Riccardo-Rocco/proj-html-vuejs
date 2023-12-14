<template>
    <div class="Title-container">
        <h4>BRAND LOGOS</h4>
    </div>
    <swiper
    :slidesPerView="5"
    :loop="true"
    :centeredSlides="true"
   
    :autoplay="{ delay: 3000, disableOnInteraction: false }"
    :modules="modules"
    class="mySwiper"
  >
      <swiper-slide><img src="../assets/images/b_logotype_1.png" alt=""></swiper-slide>
      <swiper-slide><img src="../assets/images/b_logotype_2.png" alt=""></swiper-slide><swiper-slide><img src="../assets/images/b_logotype_5.png" alt=""></swiper-slide>
      <swiper-slide><img src="../assets/images/b_logotype_3.png" alt=""></swiper-slide><swiper-slide><img src="../assets/images/b_logotype_6.png" alt=""></swiper-slide>
      <swiper-slide><img src="../assets/images/b_logotype_4.png" alt=""></swiper-slide><swiper-slide><img src="../assets/images/b_logotype_7.png" alt=""></swiper-slide>
      
    </swiper>
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
  .swiper{
    width: 80%;
    align-items: center;
  }
  .Title-container{
    text-align: center;
    margin-top: 5%;
    margin-bottom: 2%;
  }
</style>
  