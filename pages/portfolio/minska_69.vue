<template>
  <PortfolioParallax image="/images/portfolio/minska/minska2.jpg" title="Mińska 69">
    <template #content>
      <div class="Portfolio__content">
        <div class="Portfolio__description">
          <p>Nowoczesny i minimalistyczny projekt łazienki z inwestycji zlokalizowanej w Gdańsku. Szlachetna w swojej prostocie aranżacja, w której dominującymi materiałami są gresy o wzorze lastryko. Monochromatyczna kolorystyka pomieszczenia została ocieplona naturalnym fornirem drewnianym, a proste formy zmiękczone dużym okrągłym lustrem. Atmosfery wnętrzu dodaje oświetlenie, które poza spotami sufitowymi, występuje w postaci dekoracyjnej lampy wiszącej oraz liniowego oświetlenia ukrytego w przestrzeni sufitu podwieszanego.</p>
        </div>
        <div class="Portfolio_image-container">
          <img loading="lazy" :src="image2" alt="bathroom" class="Portfolio__img">
        </div>
        <div class="Portfolio_image-container">
          <div class="Portfolio__row">
            <img loading="lazy" :src="image1" alt="bathroom" class="Portfolio__img">
            <img loading="lazy" :src="image3" alt="bathroom" class="Portfolio__img">
          </div>
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
      image1: '/images/portfolio/minska/minska1.jpg',
      image2: '/images/portfolio/minska/minska2.jpg',
      image3: '/images/portfolio/minska/minska3.jpg'
    }
  }
}
</script>
