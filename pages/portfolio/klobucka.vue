<template>
  <PortfolioParallax image="/images/portfolio/klobucka/klobucka1.jpg" title="Kłobucka">
    <template #content>
      <div class="Portfolio__content">
        <div class="Portfolio__description">
          <p>Mieszkanie na warszawskim Ursynowie to przede wszystkim przemyślana i funkcjonalna przestrzeń, której aranżacja została zaprojektowana w taki sposób aby wnętrza były jednocześnie nowoczesne i stylowe. W tym niewielkim na pozór wnętrzu udało się wygospodarować miejsce na realizację funkcjonalnej kuchni z hokerami dostępnymi od strony pokoju dziennego, stół dla czterech osób oraz wygodną sofę z dodatkowym podnóżkiem, który razem z sofą może tworzyć narożnik lub stanowić niezależne siedzisko.</p>
        </div>
        <div class="Portfolio_image-container">
          <img :src="image1" alt="living-room" class="Portfolio__img">
        </div>
        <div class="Portfolio__description">
          <p>Aranżacja utrzymana jest w stonowanych i ciepłych barwach dla których tło stanowią białe ściany, a całoś dopełniają czarne dodatki elementy oświetlenia. Elegancji przestrzeni dodają płytki gresowe o marmurowym wzorze oraz stylowe, czarne lamele z obrzeżami wykończonymi w kolorze złotym. Punkt kulminacyjny stanowi oryginalna w swojej formie i kolorze sofa wraz podnóżkiem. Kolor zielony ożywia wnętrze i czyni je bardziej wyrazistym.</p>
        </div>
        <div class="Portfolio_image-container">
          <img :src="image3" alt="living-room" class="Portfolio__img">
        </div>
        <div class="Portfolio_image-container">
          <img :src="image2" alt="kitchen" class="Portfolio__img">
        </div>
        <div class="Portfolio__description">
          <p>W łazience dominuje szaro-biała tonacja, choć i tu zastosowano wyraźny akcent w postaci czarnej szafki umywalkowej oraz opraw oświetlenia mocowanych do tafli lustra. Istotnym i dominującym materiałem w tej przestrzeni jest gres o naturalnym kamiennym wzorze. Również w tym pomieszczeniu konsekwentnie postawiono na funkcjonalność wnętrza – maksymalizacje przestrzeni do przechowywania oraz ukryta w zabudowie meblowej pralka.</p>
        </div>
        <div class="Portfolio_image-container">
          <img :src="image5" alt="bathroom" class="Portfolio__img">
        </div>
        <div class="Portfolio_image-container">
          <div class="Portfolio__row">
            <img :src="image4" alt="bathroom" class="Portfolio__img">
            <img :src="image6" alt="bathroom" class="Portfolio__img">
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
      image1: '/images/portfolio/klobucka/klobucka1.jpg',
      image2: '/images/portfolio/klobucka/klobucka2.jpg',
      image3: '/images/portfolio/klobucka/klobucka3.jpg',
      image4: '/images/portfolio/klobucka/klobucka4.jpg',
      image5: '/images/portfolio/klobucka/klobucka5.jpg',
      image6: '/images/portfolio/klobucka/klobucka6.jpg'
    }
  }
}
</script>
