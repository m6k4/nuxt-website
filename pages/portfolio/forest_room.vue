<template>
  <PortfolioParallax image="/images/portfolio/forest_room/forest_room1.jpg" title="Forest Room">
    <template #content>
      <div class="Portfolio__content">
        <div class="Portfolio__description">
          <p>Projekt pokoju dziecięcego na warszawskim Mokotowie, którego motywem przewodnim jest las, zwięrzęta, zieleń oraz drewno. W aranżacji tej bardzo ciekawej przestrzeni kluczowym elementem jest łóżko, które stanowi jednocześnie rewelacyjną przestrzeń do zabaw, a nawet wspinaczki:) Na ścianie zaprojektowana została tapeta w tematyce leśnej a całość aranżacji dopełniają zabawki, meble dziecięce i akcesoria spójne z koncepcją wnętrza.</p>
        </div>
        <!-- TODO: add images -->
        <div class="Portfolio_image-container" style="padding-top: 2.5rem">
          <nuxt-img
            :lazy="true"
            format="jpg"
            :src="image1"
            alt="bathroom"
            class="Portfolio__img"
          />
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
      image1: '/images/portfolio/forest_room/forest_room1.jpg',
      image2: '/images/portfolio/forest_room/forest_room2.jpg',
      image3: '/images/portfolio/forest_room/forest_room3.jpg',
      image4: '/images/portfolio/forest_room/forest_room4.jpg'
    }
  }
}
</script>
