<template>
    <PortfolioParallax image="/images/portfolio/layla_2/layla1.jpg" title="Layla">
        <template #content>
        <div class="Portfolio1__content">
            <div class="Portfolio1__description">
            <p>Nowoczesna aranżacja łazienki w inwestycji na warszawskim Żoliborzu, gdzie istotną rolę odgrywają wysokiej jakości materiały. Wykorzystane w tej minimalistycznej przestrzeni spieki kwarcowe, o kamiennym wzorze, nadają wnętrzu elegancji i podkreślają charakter całej realizacji.</p>
            </div>
            <div class="Portfolio1_image-container">
                <div class="Portfolio1_image-container">
            <img :src="image2" alt="bathroom" class="Portfolio1__img">
            </div>
            <div class="Portfolio1__description">
            <p>Projekt utrzymany jest w odcieniach szarości z dominacją bieli i czerni. Pojawiają się również odcienie beżu, które mimo dużej ilości ciemnych elementów oraz czarnych dodatków, powodują, że przestrzeń jest ciepła w odbiorze. Dobrze i dyskretnie zaprojektowane oświetlenie oraz duże przeszklenia pozwalają zachować odpowiednią atmosferę wnętrza o każdej porze. Istotnym detalem stają się elementy sztukaterii naściennej, która odwzorowana została również na frontach szafki umywalkowej.</p>
            </div>
            <div class="Portfolio1_image-container">
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
      image1: '/images/portfolio/layla_2/layla1.jpg',
      image2: '/images/portfolio/layla_2/layla2.jpg'
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
