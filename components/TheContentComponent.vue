<template>
  <div class="TheContentComponent__wrapper">
    <div class="TheContentComponent">
        <nuxt-img
          :lazy="true"
          format="webp"
          :src="mainImage"
          alt="room"
          class="TheContentComponent__image"
          :style="isLoading ? 'opacity: 1' : 'opacity: 0'"
          height="100%"
          width="50%"
        />
        <h1 class="TheContentComponent__title" :class="{move: isScrollingOnDesktop}" :style="isLoading ? 'opacity: 1;' : 'opacity: 0;'">
          {{ title }}
        </h1>
      <div class="TheContentComponent__content" :class="{ 'show': isLoading }">
        {{ content }}
        <slot name="custom-content" />
      </div>
    </div>
    <div class="TheContentComponent__content-mobile">
      {{ content }}
      <slot name="custom-content" />
    </div>
  </div>
</template>
<script>
export default {
  name: 'TheContentComponent',
  beforeRouteEnter (to, from, next) {
    next((vm) => {
      vm.changeLoadingState()
    })
  },
  layout: 'page',
  props: {
    title: {
      type: String,
      default: ''
    },
    content: {
      type: String,
      default: ''
    },
    mainImage: {
      type: String,
      default: ''
    },
    isScrollable: {
      type: Boolean,
      default: true
    }
  },
  data () {
    return {
      isScrollingOnDesktop: false,
      isLoading: false
    }
  },
  created () {
    this.changeLoadingState()
  },
  mounted () {
    document.body.style.overflow = 'auto'
    window.addEventListener('scroll', this.handleScroll)
    this.changeLoadingState()
  },
  unmounted () {
    window.removeEventListener('scroll', this.handleScroll)
  },
  methods: {
    handleScroll () {
      if (window.innerWidth > 768) {
        if (this.isScrollable) {
          if (window.scrollY > 0) {
            this.isScrollingOnDesktop = true
          } else {
            this.isScrollingOnDesktop = false
          }
        }
      }
    },
    changeLoadingState () {
      setTimeout(() => {
        this.isLoading = true
      }, 100)
    }
  }
}
</script>
<style lang="css" scoped>
.TheContentComponent{
  height: 90vh;
  padding: 0 10%;
  position: relative;
}
.TheContentComponent__image{
  height: 100%;
  width: 50%;
  object-fit: cover;
  transition: all 1s ease-in-out
}
.TheContentComponent__title{
  font-family: 'Playfair Display', serif;
  color: black;
  position: absolute;
  top: 10%;
  left: 42%;
  text-transform: uppercase;
  font-size: 5.5rem;
  line-height: 1rem;
  font-weight: 400;
  transition: all 1.5s ease;
}
.TheContentComponent__title.move{
  top: 5%;
}

.TheContentComponent__content {
  position: absolute;
  bottom: 20%;
  font-size: 0.9rem;
  width: 35%;
  font-weight: 500;
  right: 10%;
  text-transform: uppercase;
  transition: all 2s ease;
  transform: translateX(100%);
  opacity: 0;
}

.TheContentComponent__content.show {
  transform: translateX(0);
  opacity: 1;
  transition-delay: 0.5s;
}
.TheContentComponent__custom-content {
  position: absolute;
  bottom: 20%;
  font-size: 0.9rem;
  width: 35%;
  right: 10%;
  font-weight: 500;
  text-transform: uppercase;
}
.TheContentComponent__content-mobile {
  display: none;
}

@media only screen and (max-width: 1600px) {
  .TheContentComponent__content {
    font-size: 0.8rem;
    width: 33%;
    bottom: 10%;
  }
  .TheContentComponent__title {
    font-size: 4.5rem;
  }
  .TheContentComponent__content-scroll {
    bottom: 20%
  }
}
@media only screen and (max-width: 1400px) {
  .TheContentComponent__title {
    font-size: 4rem;
  }
}
@media only screen and (max-width: 1150px) {
  .TheContentComponent {
    padding: 0;
  }
  .TheContentComponent__image {
    width: 100%;
    margin-left: 0;
    height: 95%;
    margin-top: 5%;
  }
  .TheContentComponent__wrapper {
    padding: 0 10%;
  }
  .TheContentComponent__title {
    width: 100%;
    display: flex;
    justify-content: center;
    left: auto;
    top: -3rem;
    font-size: 3.5rem;
  }
  .TheContentComponent__content {
    display: none;
  }
  .TheContentComponent__content-mobile {
    display: block;
    font-size: 0.8rem;
    margin: 4rem 0 5rem 0
  }
}
@media only screen and (max-width: 750px) {
  .TheContentComponent {
    margin-top: 0;
  }
  .TheContentComponent__wrapper {
    padding: 0;
  }
  .TheContentComponent__title {
    font-size: 6vh;
    position: absolute;
    bottom: 13.7vh;
    top: auto
  }
  .TheContentComponent__content-mobile {
    padding: 0 5%;
    margin-top: 0;
  }
  .TheContentComponent__image {
    position: absolute;
    height: 82vh;
    top: 0;
    margin-top: -10vh;
  }
}
@media only screen and (max-width: 440px) {
   .TheContentComponent__title {
    font-size: 5vh;
    bottom: 14.2vh;
  }
}

</style>
