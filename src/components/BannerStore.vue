<template>
  <!-- Women Banner Section Begin -->
  <section class="women-banner spad">
    <div class="container-fluid">
      <div class="row">
        <div class="col-lg-12 mt-5">
          <carousel class="product-slider" :wrapAround="true" :itemsToShow="3" :itemsToScroll="true" :autoplay="3000">
            <Slide v-for="(product, index) in products" :key="index">
              <div class="product-item">
                <div class="pi-pic">
                  <img :src="`/img/products/women-${index+1}.jpg`" alt="" />
                  <ul>
                    <li class="w-icon active">
                      <a href="#"><i class="icon_bag_alt"></i></a>
                    </li>
                    <li class="quick-view">
                      <a href="product.html">+ Quick View</a>
                    </li>
                  </ul>
                </div>
                <div class="pi-text">
                  <div class="catagory-name">{{ product.Category }}</div>
                  <a href="#">
                    <h5>{{ product.Name }}</h5>
                  </a>
                  <div class="product-price">
                    {{ product.PriceAfter }}
                    <span>{{ product.PriceBefore ? product.PriceBefore : '' }}</span>
                  </div>
                </div>
              </div>
            </Slide>

            <template #addons>
              <pagination />
            </template>
          </carousel>
        </div>
      </div>
    </div>
  </section>
  <!-- Women Banner Section End -->
</template>

<script>
import 'vue3-carousel/dist/carousel.css';
import {Carousel, Slide, Pagination} from 'vue3-carousel';

export default {
  name: 'BannerStore',
  components: {
    Carousel,
    Slide,
    Pagination
  },
  data() {
    return {
        products: [
            {
                Category: "Coat",
                Name: "Mickey Baggy",
                PriceAfter: "$14.00",
                PriceBefore: "$35.00"
            },
            {
                Category: "Shoes",
                Name: "Guangzhou sweater",
                PriceAfter: "$13.00",
                PriceBefore: ""
            },
            {
                Category: "Towel",
                Name: "Pure Pineapple",
                PriceAfter: "34.00",
                PriceBefore: ""
            },
            {
                Category: "Towel",
                Name: "Converse Shoes",
                PriceAfter: "$76.95",
                PriceBefore: "$137.00"
            },
        ]
    }
  }
};
</script>

<style scoped>
.product-item {
    margin-right: 25px;
}
</style>