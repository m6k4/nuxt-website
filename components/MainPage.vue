<template>
  <div class="MainPage">
    <img
      loading="lazy"
      :src="image"
      alt="background image with living room"
      :style="isLoading ? 'opacity: 1' : 'opacity: 0'"
    >
    <div class="MainPage__title" :style="isLoading ? 'top: 2rem' : 'top: 0'">
      <p>przestrzen.</p>
      <p>swiatlo.</p>
      <p>proporcja.</p>
    </div>
    <div :class="`MainPage__content ${!isLoading && 'MainPage__content-animate'}`">
      Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries.
    </div>
  </div>
</template>
<script>
export default {
  name: 'MainPage',
  data () {
    return {
      image: '/images/main.jpeg',
      isLoading: false
    }
  },
  created () {
    this.changeLoadingState()
  },
  mounted () {
    this.changeLoadingState()
  },

  methods: {
    changeLoadingState () {
      setTimeout(() => {
        this.isLoading = true
      }, 100)
    }
  }
}
</script>
<style lang="css" scoped>
.MainPage {
  height: 90vh;
  width: 100%;
  justify-content: center;
  align-items: center;
  position: relative;
  overflow-y: hidden;
}
.MainPage img {
  height: 100%;
  display: block;
  margin: 0 auto;
  transition: all 1s ease-in-out
}
.MainPage__title {
  font-family: 'Playfair Display', serif;
  color: black;
  position: absolute;
  left: 8rem;
  text-transform: uppercase;
  font-size: 4.5vw;
  line-height: 1rem;
  transition: all 1.5s ease-in-out
}
.MainPage__content {
  position: absolute;
  bottom: 15rem;
  font-size: 0.9rem;
  width: 40%;
  font-weight: 500;
  text-transform: uppercase;
  transition: all 1.5s ease-in-out;
  right: 5rem ;
  opacity: 1
}
.MainPage__content-animate {
  right: 0;
  opacity: 0;
}
@media only screen and (max-width: 1600px) {
  .MainPage__content {
    font-size: 0.8rem;
  }
}
@media only screen and (max-width: 750px) {
  .MainPage__title {
    font-size: 2rem;
    left: 2rem;
  }
  .MainPage__content {
    right: 1rem;
    bottom: 5rem;
  }
}
</style>
