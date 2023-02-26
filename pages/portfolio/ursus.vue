<template>
  <PortfolioParallax image="/images/portfolio/ursus/ursus4.jpg" title="Ursus">
    <template #content>
      <div class="Portfolio__content">
        <div class="Portfolio__description">
          <p>Ursus – niegdyś dzielnica Warszawy o typowo industrialnym charakterze, kojarzona z licznymi zakładami produkcyjnymi. Dziś jest to miejsce w trakcie przemiany, która postępuje w ekspresowym tępie. Dzielnica staje się przyjazną i zaplanowaną urbanistycznie przestrzenią miejską ze zdecydowaną przewagą zabudowy mieszkaniowej.</p>
          <p>Wnętrze mieszkania zostało zaprojektowane w stylu loftowym. Industrialnego charakteru nadały wnętrzu takie materiały jak płytki z cegły rozbiórkowej oraz tynki imitujące beton. Akcenty stanowią dodatki w czarnych kolorach, a cała aranżacja została ocieplona poprzez zastosowanie drewna w wykończeniu mebli, blatu kuchennego i okładzin ściennych.</p>
        </div>
        <div class="Portfolio_image-container">
          <img :src="image2" alt="bathroom" class="Portfolio__img">
        </div>
        <div class="Portfolio_image-container">
          <div class="Portfolio__row">
            <img :src="image1" alt="bathroom" class="Portfolio__img">
            <img :src="image3" alt="bathroom" class="Portfolio__img">
          </div>
        </div>
        <div class="Portfolio__description">
          <p>W realizacji inwestycji wykorzystano oświetlenie belgijskiej marki Wever & Ducre. Szklane, dymione klosze  skomponowane z trzech rozmiarów lamp wiszących serii Wetro nadaje części salonowej troche 'błysku’, natomiast lampy z serii Roomor zawieszone nad blatem kuchennym utrzymują swoją formą i matowym wykończeniem charakter wnętrza.</p>
        </div>
        <div class="Portfolio_image-container">
          <img :src="image4" alt="bathroom" class="Portfolio__img">
        </div>
        <div class="Portfolio_image-container" style="padding: 2.5rem 0;">
          <img :src="image5" alt="bathroom" class="Portfolio__img">
        </div>
        <div class="Portfolio_image-container">
          <img :src="image6" alt="bathroom" class="Portfolio__img">
        </div>
        <div class="Portfolio__description">
          <p>Nieocenione stały się jednak lampy Roomor na sztywnym połączeniu zwieszane nad szafkami nocnymi w pomieszczeniu sypialni. Ich forma idealnie wpisała się koncepcję zabudowy meblowej jaka została przedstawiona przez klientów w wytycznych do realizacji projektu..</p>
        </div>
        <div class="Portfolio_image-container">
          <img :src="image7" alt="bathroom" class="Portfolio__img">
        </div>
        <div class="Portfolio_image-container">
          <div class="Portfolio__row">
            <img :src="image8" alt="bathroom" class="Portfolio__img">
            <img :src="image9" alt="bathroom" class="Portfolio__img">
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
      image1: '/images/portfolio/ursus/ursus5.jpg',
      image2: '/images/portfolio/ursus/ursus6.jpg',
      image3: '/images/portfolio/ursus/ursus3.jpg',
      image4: '/images/portfolio/ursus/ursus4.jpg',
      image5: '/images/portfolio/ursus/ursus1.jpg',
      image6: '/images/portfolio/ursus/ursus1.jpg',
      image7: '/images/portfolio/ursus/ursus7.jpg',
      image8: '/images/portfolio/ursus/ursus8.jpg',
      image9: '/images/portfolio/ursus/ursus9.jpg'
    }
  }
}
</script>
