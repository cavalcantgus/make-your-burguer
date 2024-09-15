<template>
  <carousel :items-to-show="2.95" :wrapAround="true" :transition="500">
    <slide v-for="slide in images" :key="slide">
      <div class="carousel-item">
        <img :src="slide" alt="">
      </div>
    </slide>

    <template #addons>
      <navigation />
      <pagination class="custom-pagination"/>
    </template>
  </carousel>
</template>

<script>
import 'vue3-carousel/dist/carousel.css'
import { Carousel, Slide, Pagination, Navigation } from 'vue3-carousel'
import miniBurger from '/public/img/mini-burger.jpg';

export default {
  name: 'Carrossel',
  components: {
    Carousel,
    Slide,
    Pagination,
    Navigation,
  },
  data() {
    return {
        images: [
            miniBurger,
            miniBurger,
            miniBurger,
            miniBurger,
            miniBurger,
        ]
    }
  }
}
</script>

<style scoped>
.carousel__slide {
  padding: 5px;
}

.carousel__viewport {
  perspective: 2000px;
}

.carousel__track {
  transform-style: preserve-3d;
}

.carousel__slide--sliding {
  transition: 0.5s;
}

.carousel__slide {
  opacity: 0.9;
  transform: rotateY(-20deg) scale(0.85);
}

.carousel__slide--active {
  transform: rotateY(20deg) scale(0.90);
}

.carousel__slide--prev {
  opacity: 1;
  transform: rotateY(-30deg) scale(0.90);
  z-index: 1;
}

.carousel__slide--next {
  opacity: 1;
  transform: rotateY(30deg) scale(0.90);
  z-index: 1;
}

.carousel__slide--active {
  opacity: 1;
  transform: rotateY(0) scale(1.1);
  z-index: 10;
}

:deep(.custom-pagination .carousel__pagination-button::after) {
    width: 18px;
    background-color: #dbac0f;
    height: 5px;
    border-radius: 50px;
    transition: background-color 0.3s;
}

:deep(.custom-pagination .carousel__pagination-button--active::after) {
     background-color: #f77700;
}

</style>