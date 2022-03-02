<template>
  <div class="clients-section">
    <h2>Clientes</h2>
    <div class="swiper-clients">
      <div class="swiper-wrapper">
        <div class="swiper-slide">
          Boticário
        </div>
        <div class="swiper-slide">
          Petrobrás
        </div>
      </div>
      <!-- Add Pagination -->
      <div class="swiper-clients-pagination"></div>
    </div>
  </div>
</template>
<script>
import 'swiper/swiper-bundle.css';
import Swiper from 'swiper';
export default {
  beforeMount () {
    new Swiper('.swiper-clients', {
      pagination: {
        el: '.swiper-clients-pagination',
        dynamicBullets: true,
      },
    });
  }
}
</script>

<style lang="scss" scoped>
.clients-section {
  h2 {
    margin-bottom: 32px;
  }

  .swiper-clients {
    width: 600px;
    margin: auto;
  }
}
</style>
