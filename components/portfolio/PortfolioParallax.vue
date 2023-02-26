<template>
  <div class="PortfolioParallax">
    <div class="PortfolioParallax__parallax" :style="{ backgroundImage: 'url(' + image + ')' }" />
    <div class="PortfolioParallax__parallax-title">
      <h1>{{ title }}</h1>
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
  }

}
</script>
<style lang="css" scoped>
.PortfolioParallax {
  padding: 0 10%;

}

.PortfolioParallax__parallax {
  min-height: 100vh;
  background-attachment: fixed;
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
}

.PortfolioParallax__parallax-title {
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

.PortfolioParallax__parallax-title h1 {
  margin: 0;
  padding: 0;
  font-size: 6rem;
}

</style>
