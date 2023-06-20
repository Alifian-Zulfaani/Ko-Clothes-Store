<template>
  <!-- Hero Section Begin -->
  <section class="hero-section">
    <carousel :items-to-show="1" :wrap-around="true">
      <slide v-for="slide in 3" :key="slide">
        <div
          class="single-hero-items set-bg"
          :style="`background-image: url('/img/hero-${slide}.jpg')`"
        >
          <div class="container">
            <div class="row banner-info">
              <div class="col-lg-5">
                <span>Bag, kids</span>
                <h1>Black friday</h1>
                <p>
                  Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed
                  do eiusmod tempor incididunt ut labore et dolore
                </p>
                <a href="#" class="primary-btn">Shop Now</a>
              </div>
            </div>
          </div>
        </div>
      </slide>

      <template #addons>
        <navigation />
        <pagination />
      </template>
    </carousel>
  </section>
  <!-- Hero Section End -->
</template>

<script>
import 'vue3-carousel/dist/carousel.css';
import {Carousel, Slide, Pagination, Navigation} from 'vue3-carousel';

export default {
  name: 'HeroStore',
  components: {
    Carousel,
    Slide,
    Pagination,
    Navigation
  },
};
</script>

<style scoped>
.set-bg {
    width: 100%;
    height: 500px;
}
.banner-info {
    margin-top: 130px;
}
</style>
