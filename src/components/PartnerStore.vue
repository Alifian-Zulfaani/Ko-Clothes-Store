<template>
  <!-- Partner Logo Section Begin -->
  <div class="partner-logo">
    <div class="container">
      <carousel class="logo-carousel" :wrap-around="true" :autoplay="3000" :items-to-show="5">
        <slide v-for="slide in 5" :key="slide">
          <div class="logo-item">
            <div class="tablecell-inner">
              <img :src="`img/logo-carousel/logo-${slide}.png`" alt="" />
            </div>
          </div>
        </slide>

        <template #addons>
        </template>
      </carousel>
    </div>
  </div>
  <!-- Partner Logo Section End -->
</template>

<script>
import 'vue3-carousel/dist/carousel.css';
import {Carousel, Slide} from 'vue3-carousel';

export default {
  name: 'PartnerStore',
  components: {
    Carousel,
    Slide
  },
};
</script>

<style scoped>
.logo-item {
    margin-right: 50px;
}
</style>
