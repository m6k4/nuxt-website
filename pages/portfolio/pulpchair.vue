<template>
  <PortfolioParallax image="/images/portfolio/pulp_chair/pulp_chair1.jpg" title="Pulp chair">
    <template #content>
      <div class="Portfolio__content">
        <div class="Portfolio__description">
          <p>Projekt jednej z łazienek w domu jednorodzinnym w Ursusie. Efekt pracy z klientami otwartymi na kreatywne rozwiązania materiałowe i kolorystyczne zaowocował połączeniem żółtej mozaiki oraz różowego sufitu. Kolory zostały zestawione z monochromatycznym gresem o kamiennym wzorze, a cała aranżacja ozdobiona złotymi akcentami.</p>
        </div>
        <div class="Portfolio_image-container">
          <div class="Portfolio__row">
            <nuxt-img
              :lazy="true"
              format="jpg"
              :src="image1"
              alt="bathroom"
              class="Portfolio__img"
            />
            <nuxt-img
              :lazy="true"
              format="jpg"
              :src="image2"
              alt="bathroom"
              class="Portfolio__img"
            />
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
      image1: '/images/portfolio/pulp_chair/pulp_chair1.jpg',
      image2: '/images/portfolio/pulp_chair/pulp_chair2.jpg'
    }
  }
}
</script>
