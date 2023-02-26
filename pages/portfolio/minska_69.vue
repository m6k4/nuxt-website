<template>
  <PortfolioParallax image="/images/portfolio/minska/minska2.jpg" title="Mińska 69">
    <template #content>
      <div class="Portfolio1__content">
        <div class="Portfolio1__description">
          <p>Nowoczesny i minimalistyczny projekt łazienki z inwestycji zlokalizowanej w Gdańsku. Szlachetna w swojej prostocie aranżacja, w której dominującymi materiałami są gresy o wzorze lastryko. Monochromatyczna kolorystyka pomieszczenia została ocieplona naturalnym fornirem drewnianym, a proste formy zmiękczone dużym okrągłym lustrem. Atmosfery wnętrzu dodaje oświetlenie, które poza spotami sufitowymi, występuje w postaci dekoracyjnej lampy wiszącej oraz liniowego oświetlenia ukrytego w przestrzeni sufitu podwieszanego.</p>
        </div>
        <div class="Portfolio1_image-container">
          <img :src="image2" alt="bathroom" class="Portfolio1__img">
        </div>
        <div class="Portfolio1_image-container">
          <div class="Portfolio1__row">
            <img :src="image1" alt="bathroom" class="Portfolio1__img">
            <img :src="image3" alt="bathroom" class="Portfolio1__img">
          </div>
        </div>
      </div>
    </template>
  </PortfolioParallax>
</template>
<script>
import PortfolioParallax from '~/components/portfolio/PortfolioParallax.vue'

export default {
  name: 'ContactPage',
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
</style>
