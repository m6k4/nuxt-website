<template>
  <div class="PortfolioParallax" :style="isLoading ? 'opacity: 1' : 'opacity: 0'">
    <div class="PortfolioParallax__parallax" :style="{ backgroundImage: 'url(' + image + ')' }">
      <div class="PortfolioParallax__parallax-title">
        <h1>{{ title }}</h1>
      </div>
    </div>
    <slot name="content" />
  </div>
</template>
<script>

export default {
  name: 'PortfolioParallax',
  props: {
    image: {
      type: String,
      required: true
    },
    title: {
      type: String,
      required: true
    }
  },
  data () {
    return {
      isLoading: false
    }
  },
  mounted () {
    this.changeLoadingState()
  },

  methods: {
    changeLoadingState () {
      setTimeout(this.isLoading = true, 100)
    }
  }

}
</script>
<style lang="css" scoped>
.PortfolioParallax {
  padding: 0 10%;
  transition: all 1.5s ease-in-out
}

.PortfolioParallax__parallax {
  min-height: 100vh;
  background-attachment: fixed;
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  position: relative;
  object-fit: cover;
}

.PortfolioParallax__parallax-title {
  font-family: 'Playfair Display', serif;
  color: black;
  padding: 2rem;
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate3d(-50%, -50%, 0);
  font-size: 5rem;
  text-align: center;
  z-index: 1;
  color: #fff;
}

.PortfolioParallax__parallax-title h1 {
  margin: 0;
  padding: 0;
  font-size: 6rem;
  font-weight: 400;
}
@media only screen and (max-width: 1150px) {
  .PortfolioParallax__parallax-title h1{
    font-size: 5rem;
  }
}
@media only screen and (max-width: 850px) {
  .PortfolioParallax__parallax-title h1{
    font-size: 4rem;
  }
}
@media only screen and (max-width: 750px) {
  .PortfolioParallax__parallax {
    margin-top: -10vh;
    background-attachment: scroll;
  }
  .PortfolioParallax {
    padding: 0;
  }
}

@media only screen and (max-width: 576px) {
  .PortfolioParallax__parallax-title h1{
    font-size: 3rem;
  }
  .PortfolioParallax {
    padding: 0
  }
}
</style>
