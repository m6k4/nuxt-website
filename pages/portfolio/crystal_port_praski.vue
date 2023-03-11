<template>
  <PortfolioParallax image="/images/portfolio/crystal_port_praski/crystal_port_praski3.jpg" title="Crystal Port Praski">
    <template #content>
      <div class="Portfolio__content">
        <div class="Portfolio__description">
          <p>Himalaya Crystal to nazwa serii spieków kwarcowych od producenta NEOLITH. Materiał ten stał się inspiracją przy aranżacji przestrzeni aneksu kuchennego w apartamencie na warszawskiej Pradze. Połączenie jasnego, kryształowego spieku o charakterystycznym złoto-miedzianym użyłowaniu z różowym wykończeniem szafek wiszących, nadało subtelny i elegancki efekt całej zabudowie kuchennej.</p>
        </div>
        <div class="Portfolio_image-container">
          <img loading="lazy" :src="image2" alt="bathroom" class="Portfolio__img">
        </div>
        <div class="Portfolio_image-container" style="padding-top: 2.5rem">
          <img loading="lazy" :src="image1" alt="bathroom" class="Portfolio__img">
        </div>
      </div>
    </template>
  </PortfolioParallax>
</template>
<script>
import PortfolioParallax from '~/components/portfolio/PortfolioParallax.vue'

export default {
  name: 'PortfolioSinglePage',
  components: {
    PortfolioParallax
  },
  layout: 'page',
  data () {
    return {
      image1: '/images/portfolio/crystal_port_praski/crystal_port_praski1.jpg',
      image2: '/images/portfolio/crystal_port_praski/crystal_port_praski2.jpg'
    }
  }
}
</script>
