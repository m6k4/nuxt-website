<template>
  <div
    v-if="isScrollable"
    role="button"
    class="ArrowToScroll__arrow"
    :class="arrowRotationClass"
    @click="scrollTo"
  >
    <img loading="lazy" src="https://img.icons8.com/android/48/null/left.png" alt="arrow">
  </div>
</template>
<script>
export default {
  name: 'ArrowToScroll',
  props: {
    isScrollable: {
      type: Boolean,
      default: true
    }
  },
  data () {
    return {
      scrollY: 0
    }
  },
  computed: {
    arrowRotationClass () {
      const scrollTop = this.scrollY
      return scrollTop > 0 ? 'ArrowToScroll__arrow-top' : 'ArrowToScroll__arrow-bottom'
    }
  },
  mounted () {
    if (window.innerWidth > 768) {
      window.addEventListener('scroll', this.handleScroll)
    }
  },
  unmounted () {
    window.removeEventListener('scroll', this.handleScroll)
  },
  methods: {
    handleScroll () {
      if (window.innerWidth > 768) {
        this.scrollY = window.scrollY
      }
    },
    scrollTo () {
      const scrollTop = window.scrollY
      const viewportHeight = window.innerHeight
      const scrollPosition = scrollTop > 0 ? 0 : viewportHeight
      window.scrollTo({
        top: scrollPosition,
        behavior: 'smooth'
      })
    }
  }
}
</script>
<style lang="css" scoped>
.ArrowToScroll__arrow {
  position: fixed;
  bottom: 4rem;
  right: 4rem;
  z-index: 3;
  cursor: pointer;
  filter: invert(0.25);
  transition: 0.3s all;
}
.ArrowToScroll__arrow-top{
  transform: rotate(90deg);
  filter: invert(0.25);
}

.ArrowToScroll__arrow-bottom {
  transform: rotate(-90deg);
  filter: invert(0.7);
}

.ArrowToScroll__arrow:hover {
  filter: invert(0);
}
@media only screen and (max-width: 1600px) {
  .ArrowToScroll__arrow {
    width: 40px;
    height: 40px;
  }
  .ArrowToScroll__arrow img {
    width: 100%;
    height: 100%;
  }
}

@media only screen and (max-width: 1150px) {
  .ArrowToScroll__arrow {
    display: none;
  }
}
</style>
