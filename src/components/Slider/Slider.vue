<template>
  <Swiper
    ref="{swiperRef}"
    :updateOnWindowResize="true"
    :slidesPerView="windowWidth > 768 ? 3 : 1"
    :centeredSlides="true"
    :navigation="windowWidth > 1101 ? true : false"
    :loop="true"
    class="mySwiper"
  >
    <SwiperSlide><img src="@/assets/comment.png" alt="comment"/></SwiperSlide>
    <SwiperSlide><img src="@/assets/comment.png" alt="comment"/></SwiperSlide>
    <SwiperSlide><img src="@/assets/comment.png" alt="comment"/></SwiperSlide>
    <SwiperSlide><img src="@/assets/comment.png" alt="comment"/></SwiperSlide>
    <SwiperSlide><img src="@/assets/comment.png" alt="comment"/></SwiperSlide>
    <SwiperSlide><img src="@/assets/comment.png" alt="comment"/></SwiperSlide>
    <SwiperSlide><img src="@/assets/comment.png" alt="comment"/></SwiperSlide>
    <SwiperSlide><img src="@/assets/comment.png" alt="comment"/></SwiperSlide>
    <SwiperSlide><img src="@/assets/comment.png" alt="comment"/></SwiperSlide>
  </Swiper>
</template>

<script>
import SwiperCore, { Pagination, Navigation } from "swiper/core";
import { Swiper, SwiperSlide } from "swiper/vue";

import "swiper/swiper.scss";

import "swiper/components/pagination/pagination.min.css";
import "swiper/components/navigation/navigation.min.css";

import "./slider.scss";

SwiperCore.use([Pagination, Navigation]);

export default {
  name: "Slider",
  components: {
    Swiper,
    SwiperSlide,
  },
  data() {
    return {
      windowWidth: 0,
    };
  },
  created() {
    window.addEventListener("resize", this.handleResize);
    this.handleResize();
  },
  destroyed() {
    window.removeEventListener("resize", this.handleResize);
  },
  methods: {
    handleResize() {
      this.windowWidth = window.innerWidth;
    },
  },
};
</script>

<style lang="scss" scoped>
@import "./slider.scss";
img {
  width: 250px;
}
</style>
