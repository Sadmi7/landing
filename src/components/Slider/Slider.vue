<template>
  <Swiper
    ref="{swiperRef}"
    :slidesPerView="3"
    :centeredSlides="true"
    :spaceBetween="30"
    :pagination="{
      type: 'fraction',
    }"
    :navigation="true"
    class="mySwiper"
  >
    <SwiperSlide>Slide 1</SwiperSlide>
    <SwiperSlide>Slide 2</SwiperSlide>
    <SwiperSlide>Slide 3</SwiperSlide>
    <SwiperSlide>Slide 4</SwiperSlide>
  </Swiper>
</template>

<script>
// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from "swiper/vue";

// Import Swiper styles
import "swiper/swiper.scss";

import "swiper/components/pagination/pagination.min.css";
import "swiper/components/navigation/navigation.min.css";

import "./slider.scss";

// import Swiper core and required modules
import SwiperCore, { Pagination, Navigation } from "swiper/core";

// install Swiper modules
SwiperCore.use([Pagination, Navigation]);

export default {
  name: "Slider",
  components: {
    Swiper,
    SwiperSlide,
  },
  data() {
    return {};
  },
  methods: {},
};
</script>
