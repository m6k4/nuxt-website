<template>
  <div class="ThePage">
    <TheNavbar class="TheNavbar" />
    <Nuxt />
    <TheFooter class="TheFooter" />
  </div>
</template>
<script>
import TheNavbar from '~/components/TheNavbar'
import TheFooter from '~/components/TheFooter'

export default {
  name: 'ThePage',
  components: {
    TheNavbar,
    TheFooter
  }
}
</script>
<style lang="css" scoped>
.ThePage {
  position: relative;
  overflow-x: hidden;
  font-family: 'Montserrat', sans-serif;
  background-color: #F0F0F0;
  display: flex;
  flex-direction: column;
  min-height: 100vh;
}

.TheFooter {
  position: absolute;
  bottom: 0;
  width: 100%;
  background-color: #F0F0F0;
  z-index: 1;
}
</style>
<style lang="css">
.Portfolio__image-grids {
  padding: 0 10%;
}
.Portfolio__img{
  width: 100%;
}

.Portfolio__description {
  padding: 0 10%;
  margin: 10rem 0;
}

.Portfolio_image-container {
  margin: 2rem 0;
}

.Portfolio__row {
  width: 100%;
  display: flex;
  justify-content: space-between;
  margin: 2rem 0;
  gap: 8px;
}

.Portfolio__row img{
  width: 48%;
}

  @media only screen and (max-width: 750px) {
    .Portfolio__row {
      flex-direction: column;
      gap: 2rem;
    }

    .Portfolio__row img{
      width: 100%;
    }

    .Portfolio__description {
      padding: 0;
      margin: 2rem 0;
    }
    .Portfolio__image-grids {
      padding: 0;
    }
  }
  @media only screen and (max-width: 576px) {
      .Portfolio__description {
      padding: 1rem;
      font-size: 0.9rem;
      }
    }
</style>
