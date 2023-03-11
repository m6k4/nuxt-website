<template>
  <PortfolioParallax image="/images/portfolio/aroma_park/aroma_park5.webp" title="Aroma Park">
    <template #content>
      <div class="Portfolio__content">
        <div class="Portfolio__description">
          <p>Projekt apartamentu zlokalizowanego na warszawskiej Białołęce w inwestycji Aroma Park. Mimo niedużej powierzchni lokalu, dzięki niewielkim zmianom układu pomieszczeń, udało się zrealizować bardzo funkcjonalną i spójną wizualnie przestrzeń. Wnętrze jest wyraziste i kontrastowe a jednocześnie kameralne i przytulne. We wszystkich pomieszczeniach panuje podobna kolorystyka – dominują czerń i szarości, a duża ilość drewnianych wykończeń w różnej postaci ocieplają wnętrze.</p>
        </div>
        <div class="Portfolio_image-container">
          <nuxt-img
            :src="image6"
            :lazy="true"
            format="webp"
            alt="living room"
            class="Portfolio__img"
          />
        </div>
        <div class="Portfolio_image-container">
          <div class="Portfolio__row">
            <nuxt-img
              :lazy="true"
              format="webp"
              :src="image5"
              alt="living room"
              class="Portfolio__img"
            />
            <nuxt-img
              :lazy="true"
              format="webp"
              :src="image2"
              alt="living room"
              class="Portfolio__img"
            />
          </div>
          <div class="Portfolio__row">
            <nuxt-img
              :lazy="true"
              format="webp"
              :src="image3"
              alt="kitchen"
              class="Portfolio__img"
            />
            <nuxt-img
              :lazy="true"
              format="webp"
              :src="image4"
              alt="kitchen"
              class="Portfolio__img"
            />
          </div>
        </div>
        <div class="Portfolio__description">
          <p>W pomieszczeniu sypialni również postawiono na praktyczność i maksymalne wykorzystanie przestrzeni do przechowywania. Duża zabudowa meblowa szafy przechodząca w zabudowę meblową na ścianie za łóżkiem została zaprojektowana w czarnym kolorze z wykorzystaniem naturalnego forniru drewnianego. Fornir stanowi również wykończenie wnęk pełniących funkcję szafek nocnych, a przytulności dodaje wysokie tapicerowane wezgłowie w układzie jodełki. Na bocznych ścianach wnęki nad łóżkiem wykorzystano, spójnie komponujące się z całością aranżacji, kinkiety marki Chors.</p>
        </div>
        <div class="Portfolio_image-container">
          <nuxt-img
            :lazy="true"
            format="webp"
            :src="image1"
            alt="bedroom"
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
      image1: '/images/portfolio/aroma_park/aroma_park1.webp',
      image2: '/images/portfolio/aroma_park/aroma_park2.webp',
      image3: '/images/portfolio/aroma_park/aroma_park3.webp',
      image4: '/images/portfolio/aroma_park/aroma_park4.webp',
      image5: '/images/portfolio/aroma_park/aroma_park5.webp',
      image6: '/images/portfolio/aroma_park/aroma_park6.webp'
    }
  }
}
</script>
