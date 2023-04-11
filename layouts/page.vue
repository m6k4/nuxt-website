<template>
  <div
    class="ThePage"
    :style="{
      height: setMenuHeightForMobile()
    }"
  >
    <TheNavbar class="TheNavbar" />
    <Nuxt />
    <ArrowToScroll v-if="isArrowVisible" />
    <TheFooter class="TheFooter" />
  </div>
</template>
<script>
import TheNavbar from '~/components/TheNavbar'
import TheFooter from '~/components/TheFooter'
import ArrowToScroll from '~/components/ArrowToScroll'
import { urlWithScrollingArrow } from '~/utils/constants'

export default {
  name: 'ThePage',
  components: {
    TheNavbar,
    TheFooter,
    ArrowToScroll
  },
  computed: {
    isArrowVisible () {
      return urlWithScrollingArrow.includes(this.$route.path)
    },
    isMainPage () {
      return this.$route.path === '/'
    }
  },
  methods: {
    setMenuHeightForMobile () {
      if (typeof window !== 'undefined' && window.innerWidth < 1150 && this.isMainPage) {
        const viewportHeight = window.innerHeight
        const topBarHeight = window.visualViewport.offsetTop
        const menuHeight = viewportHeight - topBarHeight
        return `${menuHeight}px`
      }
      return ''
    }
  }
}
</script>
<style lang="css" scoped>
.ThePage {
  position: relative;
  overflow: hidden;
  font-family: 'Montserrat', sans-serif;
  background-color: #F0F0F0;
  display: flex;
  flex-direction: column;
  min-height: 100vh;
}

.TheFooter {
  position: fixed;
  bottom: 0;
  width: 100%;
  background-color: #F0F0F0;
  z-index: 1;
}

@media only screen and (max-width: 750px) {
  .ThePage {
    min-height: auto;
  }
  .TheFooter {
    display: none;
  }
}
</style>
<style lang="css">
.Portfolio__image-grids {
  padding: 0 10%;
}
@media only screen and (max-width: 1150px) {
  .ThePage {
    padding: 0;
  }

  .Portfolio {
    padding: 0;
  }

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
    .Portfolio__content {
      padding: 5%
    }
  }
  @media only screen and (max-width: 576px) {
      .Portfolio__description {
      padding: 1rem;
      font-size: 0.9rem;
      }
    }
</style>
