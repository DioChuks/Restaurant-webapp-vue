<script>
import { Swiper, SwiperSlide } from 'swiper/vue'
import { Autoplay, Pagination } from 'swiper/modules'
import 'swiper/css'
import 'swiper/css/autoplay'
import 'swiper/css/pagination'
import { ref } from 'vue'
export default {
  components: { Swiper, SwiperSlide },
  setup() {
    const swiperTextBase = ref([
      {
        subTitle: 'Welcome to our restaurant',
        title: 'gift voucher',
        text: 'give away your beloved customers',
        img: 'http://localhost:5173/src/assets/127-1279527_three-little-bears-clipart.png',
        link: '#',
        class: 'slide1'
      },
      {
        subTitle: 'sale of 10% this dish',
        title: 'the fresh',
        text: 'food restaurant',
        img: 'http://localhost:5173/src//assets/127-1279527_three-little-bears-clipart.png',
        link: '#',
        class: 'slide2'
      },
      {
        subTitle: 'we are open',
        title: 'fresh fruits',
        text: 'you will love it',
        img: 'http://localhost:5173/src//assets/127-1279527_three-little-bears-clipart.png',
        link: '#',
        class: 'slide3'
      }
    ])
    return { modules: [Pagination, Autoplay], swiperTextBase }
  }
}
</script>

<template>
  <!-- slider section start -->
  <section>
    <swiper
    :modules="modules"
    :space-between="20"
    :loop="true"
    :pagination="{ clickable: true }"
    :autoplay="{
      delay: 2500,
      disableOnInteraction: false,
      pauseOnMouseEnter: true
    }"
  >
    <swiper-slide v-for="text in swiperTextBase" :key="text.subTitle" class="home" id="home">
      <div class="home-slider">
        <div class="wrapper">
          <div class="slide" :id="text.class">
            <div class="content">
              <img :src="text.img" alt="image" width="50" />
              <h3>{{ text.subTitle }}</h3>
              <h1>{{ text.title }}</h1>
              <p>{{ text.text }}</p>
              <a :href="text.link" class="btn">order now</a>
            </div>
          </div>
        </div>
        <div class="swiper-pagination-bullet"></div>
      </div>
    </swiper-slide>
  </swiper>
  </section>
  <!-- <div class="home" id="home">
    <div class="swiper home-slider">
      <div class="swiper-wrapper wrapper">
        <div class="swiper-slide slide slide1">
          <div class="content">
            <img src="../assets/127-1279527_three-little-bears-clipart.png" alt="Utensils - Kitchen Utensil @clipartmax.com" width="50">
            <h3>delicious royate</h3>
            <h1>gift voucher</h1>
            <p>give away your beloved customers</p>
            <a href="#" class="btn">order now</a>
          </div>
        </div>
        <div class="swiper-slide slide slide2">
          <div class="content">
            <img src="../assets/127-1279527_three-little-bears-clipart.png" alt="Utensils - Kitchen Utensil @clipartmax.com" width="50">
            <h3>sale of 10% this dish</h3>
            <h1>the fresh</h1>
            <p>food restaurant</p>
            <a href="#" class="btn">order now</a>
          </div>
        </div>
        <div class="swiper-slide slide slide3">
          <div class="content">
            <img src="../assets/127-1279527_three-little-bears-clipart.png" alt="Utensils - Kitchen Utensil @clipartmax.com" width="50">
            <h3>we are open</h3>
            <h1>fresh fruits</h1>
            <p>you will love it</p>
            <a href="#" class="btn">order now</a>
          </div>
        </div>
      </div>
      <div class="swiper-pagination-bullet"></div>\
    </div>
  </div> -->
  <!-- slider section end -->
</template>

<style scoped>
</style>
