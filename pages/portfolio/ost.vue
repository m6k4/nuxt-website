<template>
  <PortfolioParallax image="/images/portfolio/ost_01/ost2.jpg" title="Ost 1">
    <template #content>
      <div class="Portfolio__content">
        <div class="Portfolio__description">
          <p>Kolorystyka tej niewielkiej przestrzeni opiera się na połączeniu drewnianych okładzin, stonowanych odcieni beżu, ciepłych szarości oraz bieli. W tym pomieszczeniu, jak i w całej inwestycji, dominują naturalne materiały wzbogacone złotymi akcentami, które nadają elegancji oraz szlachetności.</p>
          <p>Istotnym aspektem projektu jest także zróżnicowanie użytych faktur – zestawienie spieków o surowej, kamiennej strukturze z marmurowymi blatami w satynowym wykończeniu czy np. płytkami dekoracyjnymi o łagodnym reliefowym wzorze.</p>
        </div>
        <div class="Portfolio_image-container">
          <img :src="image2" alt="bathroom" class="Portfolio__img">
        </div>
        <div class="Portfolio_image-container">
          <div class="Portfolio__row">
            <img :src="image3" alt="bathroom" class="Portfolio__img">
            <img :src="image1" alt="bathroom" class="Portfolio__img">
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
      image1: '/images/portfolio/ost_01/ost1.jpg',
      image2: '/images/portfolio/ost_01/ost2.jpg',
      image3: '/images/portfolio/ost_01/ost3.jpg'
    }
  }
}
</script>
