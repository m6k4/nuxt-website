<template>
  <PortfolioParallax image="/images/portfolio/sarmacka/sarmacka1.jpg" title="Sarmacka">
    <template #content>
      <div class="Portfolio__content">
        <div class="Portfolio__description">
          <p>Są projekty, w których jeden materiał determinuje koncepcję całej aranżacji. Tak było również w przypadku tej aranżacji, której kluczowym elementem stała się wyjątkowa płytka FIO.PASSEPARTOUT. Materiał o bardzo geometrycznym, reliefowym wzorze w połączeniu z wielkoformatowym marmurowym gresem czynią to wnętrze nowoczesnym i eleganckim. Szlachetności dodaje złota armatura, lustro z zaokrąglonymi narożnikami w delikatnej czarnej ramie oraz towarzyszące mu kinkiety w pionowym układzie.</p>
        </div>
        <div class="Portfolio_image-container">
          <img :src="image2" alt="bathroom" class="Portfolio__img">
        </div>
        <div class="Portfolio_image-container">
          <div class="Portfolio__row">
            <img :src="image1" alt="bathroom" class="Portfolio__img">
            <img :src="image3" alt="bathroom" class="Portfolio__img">
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
      image1: '/images/portfolio/sarmacka/sarmacka2.jpg',
      image2: '/images/portfolio/sarmacka/sarmacka1.jpg',
      image3: '/images/portfolio/sarmacka/sarmacka3.jpg'
    }
  }
}
</script>
