<template>
  <PortfolioParallax image="/images/portfolio/t_house/t_house1.jpg" title="T House">
    <template #content>
      <div class="Portfolio__content">
        <div class="Portfolio__description">
          <p>Jasna i lekka aranżacja pokoju dziecięcego zaprojektowana w stonowanej i ciepłej kolorystyce. Zgodnie z wytycznymi klientów w pomieszczeniu znajduje się biurko oraz duża i funkcjonalna szafa. Kluczowym elementem aranżacji jest łóżko z tapicerowanym bokiem, wezgłowiem oraz fragmentem siedziska, za którym zaprojektowane zostały grafiki w formie łuków. Siedzisko będące częścią konstrukcji łóżka pełnić może także funkcję niezależnej pufy. W pokoju znalazło się również miejsce na huśtawkę oraz drabinkę do zabaw.</p>
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
              :src="image3"
              alt="bathroom"
              class="Portfolio__img"
            />
          </div>
        </div>
        <div class="Portfolio_image-container">
          <nuxt-img
            :lazy="true"
            format="jpg"
            :src="image2"
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
      image1: '/images/portfolio/t_house/t_house2.jpg',
      image2: '/images/portfolio/t_house3.jpg',
      image3: '/images/portfolio/t_house/t_house1.jpg'
    }
  }
}
</script>
