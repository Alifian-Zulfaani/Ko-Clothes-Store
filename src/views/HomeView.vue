<template>
  <div class="home">
    <HeaderStore />
    <HeroStore />
    <BannerStore />
    <GalleryStore />
    <PartnerStore />
    <FooterStore />
  </div>
</template>

<script>
// @ is an alias to /src
import HeaderStore from '@/components/HeaderStore.vue'
import HeroStore from '@/components/HeroStore.vue'
import BannerStore from '@/components/BannerStore.vue'
import GalleryStore from '@/components/GalleryStore.vue'
import PartnerStore from '@/components/PartnerStore.vue'
import FooterStore from '@/components/FooterStore.vue'

export default {
  name: 'HomeView',
  components: {
    HeaderStore,
    HeroStore,
    BannerStore,
    GalleryStore,
    PartnerStore,
    FooterStore
  },
};
</script>
