<template>
  <PortfolioParallax image="/images/portfolio/t_house/t_house1.jpg" title="T House">
    <template #content>
      <div class="Portfolio1__content">
        <div class="Portfolio1__description">
          <p>Jasna i lekka aranżacja pokoju dziecięcego zaprojektowana w stonowanej i ciepłej kolorystyce. Zgodnie z wytycznymi klientów w pomieszczeniu znajduje się biurko oraz duża i funkcjonalna szafa. Kluczowym elementem aranżacji jest łóżko z tapicerowanym bokiem, wezgłowiem oraz fragmentem siedziska, za którym zaprojektowane zostały grafiki w formie łuków. Siedzisko będące częścią konstrukcji łóżka pełnić może także funkcję niezależnej pufy. W pokoju znalazło się również miejsce na huśtawkę oraz drabinkę do zabaw.</p>
        </div>
        <div class="Portfolio1_image-container">
          <div class="Portfolio1__row">
            <img :src="image1" alt="bathroom" class="Portfolio1__img">
            <img :src="image3" alt="bathroom" class="Portfolio1__img">
          </div>
        </div>
        <div class="Portfolio1_image-container">
          <img :src="image2" alt="bathroom" class="Portfolio1__img">
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
      image2: '/images/portfolio/t_house/t_house3.jpg',
      image3: '/images/portfolio/t_house/t_house1.jpg'
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
