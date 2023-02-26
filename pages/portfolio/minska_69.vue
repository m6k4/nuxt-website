<template>
  <PortfolioParallax image="/images/portfolio/bedroom.jpg" title="Mińska 69">
    <template #content>
      <div class="Portfolio1__content">
        <div class="Portfolio1__description">
          <p>Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industrys standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries.</p>
        </div>
        <div class="Portfolio1__grid">
          <p> orem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industrys standard dummy text ever si</p>
          <img :src="sink" alt="bathroom">
        </div>
        <div class="Portfolio1__grid">
          <img :src="tv" alt="bathroom">
          <p> orem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industrys standard dummy text ever si</p>
        </div>
        <div class="Portfolio1__grid">
          <p> orem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industrys standard dummy text ever si</p>
          <img :src="whiteSink" alt="bathroom">
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
      bedroom: '/images/portfolio/bedroom.jpg',
      bathroom: '/images/portfolio/bathroom.jpg',
      sink: '/images/portfolio/sink.jpg',
      sinks: '/images/portfolio/sinks.jpg',
      whiteSink: '/images/portfolio/white_sink.jpg',
      kidsRoomGreen: '/images/portfolio/kidsroom2.jpg',
      circleMirror: '/images/portfolio/circle_mirror.jpg',
      tv: '/images/portfolio/tv.jpg',
      currentHover: null
    }
  }
}
</script>
<style lang="css" scoped>
.Portfolio1 {
  padding: 0 10%;

}

.Portfolio1__content {
  z-index: 10;
}

.Portfolio1__description {
  padding: 0 10%;
  margin: 10rem 0;
}

.Portfolio1__grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  transition: all 0.5s ease;
}

.Portfolio1__grid img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  transition: all 0.5s ease;
}

.Portfolio1__grid p {
  padding: 0 10%;
  display: flex;
  align-items: center;
  justify-content: center;
  text-align: center;
  font-size: 1.5rem;
  font-weight: 300;
  line-height: 1.5;
  color: #000;
  transition: all 0.5s ease;
}

</style>
