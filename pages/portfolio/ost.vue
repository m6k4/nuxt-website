<template>
    <PortfolioParallax image="/images/portfolio/ost_01/ost2.jpg" title="Ost 1">
        <template #content>
        <div class="Portfolio1__content">
            <div class="Portfolio1__description">
            <p>Kolorystyka tej niewielkiej przestrzeni opiera się na połączeniu drewnianych okładzin, stonowanych odcieni beżu, ciepłych szarości oraz bieli. W tym pomieszczeniu, jak i w całej inwestycji, dominują naturalne materiały wzbogacone złotymi akcentami, które nadają elegancji oraz szlachetności.</p>
            <p>Istotnym aspektem projektu jest także zróżnicowanie użytych faktur – zestawienie spieków o surowej, kamiennej strukturze z marmurowymi blatami w satynowym wykończeniu czy np. płytkami dekoracyjnymi o łagodnym reliefowym wzorze.</p>
            </div>
            <div class="Portfolio1_image-container">
            <img :src="image2" alt="bathroom" class="Portfolio1__img">
            </div>
            <div class="Portfolio1_image-container">
            <div class="Portfolio1__row">
                <img :src="image3" alt="bathroom" class="Portfolio1__img">
                <img :src="image1" alt="bathroom" class="Portfolio1__img">
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
display: flex;
gap: 3rem
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
    flex-direction: column;
    gap: 0
    }
}
</style>
