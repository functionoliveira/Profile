<template>
  <div class="references-section">
    <h2>Referências</h2>
    <div class="swiper-container">
      <div class="swiper-wrapper">
        <div class="swiper-slide">
          <brief />
        </div>
        <div class="swiper-slide">
          <brief />
        </div>
      </div>
      <!-- Add Pagination -->
      <div class="swiper-pagination"></div>
    </div>
  </div>
</template>
<script>
import 'swiper/swiper-bundle.css';
import Swiper from 'swiper';
import Brief from '~/components/brief/Brief'

export default {
  components: { Brief },
  beforeMount () {
    new Swiper('.swiper-container', {
      pagination: {
        el: '.swiper-pagination',
        dynamicBullets: true,
      },
    });
  }
}
</script>

<style lang="scss" scoped>
.references-section {
  h2 {
    margin-bottom: 32px;
  }

  .swiper-container {
    width: 900px;
    margin: auto;
  }
}
</style>
