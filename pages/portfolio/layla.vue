<template>
  <PortfolioParallax image="/images/portfolio/layla_2/layla1.jpg" title="Layla">
    <template #content>
      <div class="Portfolio__content">
        <div class="Portfolio__description">
          <p>Nowoczesna aranżacja łazienki w inwestycji na warszawskim Żoliborzu, gdzie istotną rolę odgrywają wysokiej jakości materiały. Wykorzystane w tej minimalistycznej przestrzeni spieki kwarcowe, o kamiennym wzorze, nadają wnętrzu elegancji i podkreślają charakter całej realizacji.</p>
        </div>
        <div class="Portfolio_image-container">
          <div class="Portfolio_image-container">
            <nuxt-img
              :lazy="true"
              format="jpg"
              :src="image2"
              alt="bathroom"
              class="Portfolio__img"
            />
          </div>
          <div class="Portfolio__description">
            <p>Projekt utrzymany jest w odcieniach szarości z dominacją bieli i czerni. Pojawiają się również odcienie beżu, które mimo dużej ilości ciemnych elementów oraz czarnych dodatków, powodują, że przestrzeń jest ciepła w odbiorze. Dobrze i dyskretnie zaprojektowane oświetlenie oraz duże przeszklenia pozwalają zachować odpowiednią atmosferę wnętrza o każdej porze. Istotnym detalem stają się elementy sztukaterii naściennej, która odwzorowana została również na frontach szafki umywalkowej.</p>
          </div>
          <div class="Portfolio_image-container">
            <nuxt-img
              :lazy="true"
              format="jpg"
              :src="image1"
              alt="bathroom"
              class="Portfolio__img"
            />
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
