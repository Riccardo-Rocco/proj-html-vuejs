<template>
  <Swiper :pagination="{ clickable: true,}" :modules="modules" class="mySwiper" >
    <SwiperSlide>
      <img src="../assets/images/testimonials_home_1_bg.jpg" alt="Image 1" class="d-block w-100">
      <div class="carousel-caption">
        <img src="../assets/images/man_testimonial.png" alt="" class="mb-3">
        <p>Curabitur non tristique tortor. Vestibulum aliquet suscipit ipsum in volutpat. Donec vel lacinia sem, vitae semper nulla. In hac habitasse platea dictumst. Mauris consectetur est et nibh sadip hendrerit bibendum.</p>
        <h6>Darío Pineda, Theme Fusion</h6>
      </div>
    </SwiperSlide>
    <SwiperSlide>
      <img src="../assets/images/testimonials_home_1_bg.jpg" alt="Image 2" class="d-block w-100">
      <div class="carousel-caption">
        <img src="../assets/images/woman_testimonial.png" alt="" class="mb-3">
        <p>Proin blandit metus vel magna dignissim varius. Morbi enim lorem, sollicitudin vitae ante nec, rutrum venenatis neque. In mi augue, iaculis nec dui ac, condimentum consequat velit. Ut et metus justo.</p>
        <h6>Lisa Smith, Theme Fusion</h6>
      </div>
    </SwiperSlide>
  </Swiper>
</template>

<script>
import { Swiper, SwiperSlide } from 'swiper/vue';
import 'swiper/css';
import 'swiper/css/pagination';
import { Pagination } from 'swiper/modules';

export default {
  components: {
    Swiper,
    SwiperSlide,
  },
  setup() {
    return {
      modules: [Pagination],
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
.mySwiper{margin-top: 10%;}

.carousel-caption {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  text-align: center;
  color: #fff; 
}

.carousel-caption h6 {
  font-size: 1.8em; 
}



img{
  max-height: 500px;
}

</style>
