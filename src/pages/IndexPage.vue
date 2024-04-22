<template>
  <q-page class="container-md">
    <div class="flex flex-center">
      <img
        class="q-mt-md img"
        alt="Quasar logo"
        src="~assets/camera.jpg"
      >
      <custom-carousel></custom-carousel>
    </div>
  </q-page>
</template>

<script setup>
import CustomCarousel from "src/components/CustomCarousel.vue";
defineOptions({
  name: 'IndexPage'
});
</script>

<style scoped>
  .img {
    width: 96%; 
    height: 200px; 
    object-fit: cover; 
    border-radius: 10px;
  }
</style>