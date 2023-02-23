<template>
  <div class="TheContentComponent__wrapper">
    <div class="TheContentComponent">
      <img
        :src="mainImage"
        alt="kids_room"
        class="TheContentComponent__image"
        :style="isLoading ? 'opacity: 1' : 'opacity: 0'"
      >
      <h1 class="TheContentComponent__title" :class="{move: isScrollingOnDesktop}">
        {{ title }}
      </h1>
      <div :class="`TheContentComponent__content ${isScrollable && 'TheContentComponent__content-scroll'}`" :style="isLoading ? 'opacity: 1; right: 10%;' : 'opacity: 0; right: 0;'">
        {{ content }}
        <slot name="custom-content" />
      </div>
      <div v-if="isScrollable" class="TheContentComponent__arrow" @click="scrollTo" :style="isScrollingActionSet ? 'transform: rotate(-90deg); filter: invert(0.25);' : 'transform: rotate(90deg); filter: invert(0.7);' ">
        <img src="https://img.icons8.com/android/48/null/left.png"/>
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
  layout: 'page',
  props: ['title', 'content', 'mainImage', 'isScrollable'],
  data () {
    return {
      isScrollingOnDesktop: false,
      isLoading: false,
      isScrollingActionSet: true
    }
  },
  mounted () {
    window.addEventListener('scroll', this.handleScroll)
    this.changeLoadingState()
  },
  beforeRouteEnter (to, from, next) {
    next((vm) => {
      vm.changeLoadingState()
    })
  },
  methods: {
    handleScroll () {
      if (window.innerWidth > 768) {
        if (window.scrollY > 0) {
          this.isScrollingOnDesktop = true
        } else {
          this.isScrollingOnDesktop = false
        }
      }
    },
    changeLoadingState () {
      setTimeout(this.isLoading = true, 1000)
    },
    scrollTo () {
      const currentScrollPos = window.pageYOffset || document.documentElement.scrollTop || document.body.scrollTop || 0
      console.log(currentScrollPos)
      if (currentScrollPos >= window.innerHeight) {
        window.scrollTo({ top: 0, behavior: 'smooth' })
        this.isScrollingActionSet = true
      } else {
        window.scrollTo({ top: window.innerHeight + 80, behavior: 'smooth' })
        this.isScrollingActionSet = false
      }
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
  left: 45%;
  text-transform: uppercase;
  font-size: 5rem;
  line-height: 1rem;
  font-weight: 400;
  transition: all 0.5s ease;
}
.TheContentComponent__title.move{
  top: 5%;
}

.TheContentComponent__content {
  position: absolute;
  bottom: 20%;
  font-size: 0.8rem;
  width: 35%;
  font-weight: 500;
  text-transform: uppercase;
  transition: all 1.5s ease;
}
.TheContentComponent__custom-content {
  position: absolute;
  bottom: 20%;
  font-size: 0.8rem;
  width: 35%;
  right: 10%;
  font-weight: 500;
  text-transform: uppercase;
}
.TheContentComponent__content-mobile {
  display: none;
}
.TheContentComponent__arrow {
  position: fixed;
  bottom: 4rem;
  right: 15rem;
  z-index: 3;
  cursor: pointer;
  filter: invert(0.25);
  transition: 0.3s all;
}
.TheContentComponent__arrow:hover {
  filter: invert(0);
}
@media only screen and (max-width: 1600px) {
  .TheContentComponent__content {
    font-size: 0.6rem;
    width: 33%;
    bottom: 10%;
  }
  .TheContentComponent__image {
    width: 35rem;
  }
  .TheContentComponent__title {
    font-size: 4.5rem;
  }
  .TheContentComponent__arrow {
    width: 40px;
    height: 40px;
  }
  .TheContentComponent__arrow img {
    width: 100%;
    height: 100%;
  }
  .TheContentComponent__content-scroll {
    bottom: 20%
  }
}
@media only screen and (max-width: 1400px) {
  .TheContentComponent__image {
    margin-left: 1rem;
  }
  .TheContentComponent__title {
    font-size: 4rem;
  }
}
@media only screen and (max-width: 1150px) {
  .TheContentComponent {
    background-color: #D7CAC2;
    padding: 0;
    margin-top: 5%
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
  .TheContentComponent__arrow {
    display: none;
  }
}
@media only screen and (max-width: 750px) {
  .TheContentComponent__wrapper {
    padding: 0;
  }
  .TheContentComponent__title {
    font-size: 3rem;
  }
  .TheContentComponent__content-mobile {
    padding: 0 5%;
    margin-top: 3rem;
  }
}
@media only screen and (max-width: 576px) {
  .TheContentComponent__wrapper {
    padding: 0;
  }
  .TheContentComponent__title {
    font-size: 2.5rem;
    top: -2.5rem;
  }
  .TheContentComponent__image {
    margin-top: 6%;
    height: 96%;
  }
  .TheContentComponent__content-mobile {
    font-size: 0.7rem;
  }

}
@media only screen and (max-width: 440px) {
  .TheContentComponent__title {
    font-size: 2rem;
    top: -2rem;
  }
  .TheContentComponent__image {
    margin-top: 6%;
    height: 98%;
  }
}
</style>
