<template>
  <PortfolioParallax image="/images/portfolio/two_side/two_side4.jpg" title="Two side">
    <template #content>
      <div class="Portfolio__content">
        <div class="Portfolio__description">
          <p>
            Zdarza się, że klienci mają podzielone upodobania i oczekiwania co do aranżacji projektowanych przestrzeni. W tej inwestycji, a konkretnie
            w pomieszczeniu sypialni, zadaniem było połączenie kolorów, detalu sztukaterii, złotych akcentów z bardziej surowym, ciemnym
            i minimalistycznym stylem aranżacji.
          </p>
          <p>Dominującym kolorem jest zieleń, która ozdobiona sztukaterią naścienną czyni wnętrze eleganckim. Szlachetności dodają złote akcenty oraz wykorzystanie naturalnego drewna w wykończeniu szafek nocnych. Ciemna zabudowa meblowa kontrastuje z zasłonami w jasnym różowym kolorze, które razem z tapicerowanym wezgłowiem ocieplają aranżację.</p>
        </div>
        <div class="Portfolio_image-container">
          <div class="Portfolio__row">
            <img loading="lazy" :src="image1" alt="bathroom" class="Portfolio__img">
            <img loading="lazy" :src="image3" alt="bathroom" class="Portfolio__img">
          </div>
        </div>
        <div class="Portfolio_image-container">
          <img loading="lazy" :src="image4" alt="bathroom" class="Portfolio__img">
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
      image1: '/images/portfolio/two_side/two_side1.jpg',
      image2: '/images/portfolio/two_side/two_side2.jpg',
      image3: '/images/portfolio/two_side/two_side3.jpg',
      image4: '/images/portfolio/two_side/two_side4.jpg'
    }
  }
}
</script>
