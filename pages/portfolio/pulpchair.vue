<template>
    <PortfolioParallax image="/images/portfolio/pulp_chair/pulp_chair1.jpg" title="Pulp chair">
        <template #content>
        <div class="Portfolio1__content">
            <div class="Portfolio1__description">
            <p>Projekt jednej z łazienek w domu jednorodzinnym w Ursusie. Efekt pracy z klientami otwartymi na kreatywne rozwiązania materiałowe i kolorystyczne zaowocował połączeniem żółtej mozaiki oraz różowego sufitu. Kolory zostały zestawione z monochromatycznym gresem o kamiennym wzorze, a cała aranżacja ozdobiona złotymi akcentami.</p>
            </div>
            <div class="Portfolio1_image-container">
            <div class="Portfolio1__row">
                <img :src="image1" alt="bathroom" class="Portfolio1__img">
                <img :src="image2" alt="bathroom" class="Portfolio1__img">
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
