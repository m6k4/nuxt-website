<template>
  <div class="Portfolio1">
    <div class="Portfolio1__parallax" />
    <div class="Portfolio1__parallax-title">
      <h1>Mińska 69</h1>
    </div>
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
  </div>
</template>
<script>

export default {
  name: 'ContactPage',
  components: {
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

.Portfolio1__parallax {
  background-image: url('/images/portfolio/bedroom.jpg');
  min-height: 100vh;
  background-attachment: fixed;
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
}

.Portfolio1__parallax-title {
  font-family: 'Playfair Display', serif;
  color: black;
  font-size: 5rem;
  line-height: 1rem;
  padding: 2rem;
  position: absolute;
  top: 14%;
  left: 50%;
  transform: translate(-50%, -50%);
  font-size: 5rem;
  font-weight: 300;
  text-align: center;
  z-index: 9;
  color: #fff
}

.Portfolio1__parallax-title h1 {
  margin: 0;
  padding: 0;
  font-size: 6rem;
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
