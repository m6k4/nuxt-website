<template>
  <PortfolioParallax image="/images/portfolio/crystal_port_praski/crystal_port_praski3.jpg" title="Crystal Port Praski">
    <template #content>
      <div class="Portfolio1__content">
        <div class="Portfolio1__description">
          <p>Himalaya Crystal to nazwa serii spieków kwarcowych od producenta NEOLITH. Materiał ten stał się inspiracją przy aranżacji przestrzeni aneksu kuchennego w apartamencie na warszawskiej Pradze. Połączenie jasnego, kryształowego spieku o charakterystycznym złoto-miedzianym użyłowaniu z różowym wykończeniem szafek wiszących, nadało subtelny i elegancki efekt całej zabudowie kuchennej.</p>
        </div>
        <div class="Portfolio1_image-container">
          <img :src="image2" alt="bathroom" class="Portfolio1__img">
        </div>
        <div class="Portfolio1_image-container" style="padding-top: 2.5rem">
          <img :src="image1" alt="bathroom" class="Portfolio1__img">
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
<style lang="css" scoped>
.Portfolio1 {
  padding: 0 10%;

}

.Portfolio1__img{
  width: 100%;
}

.Portfolio1__description {
  padding: 0 10%;
  margin: 10rem 0;
}

.Portfolio1__row {
  width: 100%;
  display: flex;
  justify-content: space-between;
  margin: 2rem 0;
  gap: 8px;
}

.Portfolio1__row img{
  width: 48%;
}

  @media only screen and (max-width: 750px) {
    .Portfolio1__row {
      flex-direction: column;
      gap: 2rem;
    }

    .Portfolio1__row img{
      width: 100%;
    }

    .Portfolio1__description {
      padding: 0;
      margin: 2rem 0;
    }
  }
@media only screen and (max-width: 576px) {
    .Portfolio1__description {
    padding: 1rem;
    font-size: 0.9rem;
    }
}
</style>
