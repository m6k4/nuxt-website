<template>
<PortfolioParallax image="/images/portfolio/sarmacka/sarmacka1.jpg" title="Sarmacka">
    <template #content>
    <div class="Portfolio1__content">
        <div class="Portfolio1__description">
        <p>Są projekty, w których jeden materiał determinuje koncepcję całej aranżacji. Tak było również w przypadku tej aranżacji, której kluczowym elementem stała się wyjątkowa płytka FIO.PASSEPARTOUT. Materiał o bardzo geometrycznym, reliefowym wzorze w połączeniu z wielkoformatowym marmurowym gresem czynią to wnętrze nowoczesnym i eleganckim. Szlachetności dodaje złota armatura, lustro z zaokrąglonymi narożnikami w delikatnej czarnej ramie oraz towarzyszące mu kinkiety w pionowym układzie.</p>
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
font-size: 1rem;
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
