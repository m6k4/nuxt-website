<template>
  <div class="TheNavbar">
    <div class="TheNavbar__navbar" :style="isScrollHidden ? 'transform: translate3d(0, -10vh, 0)' : ''">
      <div class="TheNavbar__logo">
        <TheLogo />
      </div>
      <div class="TheNavbar__navbar-buttons">
        <NuxtLink to="/portfolio">
          <span :class="{ active: activeTab === 'portfolio' }" @click="activeTab = 'portfolio'">Portfolio</span>
        </NuxtLink>
        <NuxtLink to="/navy">
          <span :class="{ active: activeTab === 'navy' }" @click="activeTab = 'navy'">Navy</span>
        </NuxtLink>
        <NuxtLink to="/offer">
          <span :class="{ active: activeTab === 'offer' }" @click="activeTab = 'offer'">Oferta</span>
        </NuxtLink>
        <NuxtLink to="/contact">
          <span :class="{ active: activeTab === 'contact' }" @click="activeTab = 'contact'">Kontakt</span>
        </NuxtLink>
      </div>
      <div class="TheNavbar__icons">
        <a
          href="https://facebook.com"
          class="facebook"
          target="_blank"
        >
          <img loading="lazy" :src="facebook" alt="facebook icon">
        </a>
        <a
          href="https://instagram.com"
          class="instagram"
          target="_blank"
        >
          <img loading="lazy" :src="instagram" alt="instagram icon">
        </a>
      </div>
    </div>
    <div class="TheNavbar__mobile">
      <div class="TheNavbar__logo">
        <TheLogo />
      </div>
      <div style="position: relative; z-index: 11;" :class="showMore ? 'TheNavbar__menu open' : 'TheNavbar__menu'" @click="toggleMenu">
        <div class="TheNavbar__menu-burger" />
      </div>
    </div>
    <div
      class="TheNavbar__mobile-content"
      :style="{
        transform: `translateY(${showMore ? '0' : '-' + setMenuHeightForMobile()})`,
        position: 'fixed',
      }"
    >
      <div class="TheNavbar__mobile-buttons" :style="!showMore && 'margin-top: -10rem'">
        <NuxtLink to="/portfolio">
          <span :class="{ active: activeTab === 'portfolio' }" @click="changeTab('portfolio')">Portfolio</span>
        </NuxtLink>
        <NuxtLink to="/navy">
          <span :class="{ active: activeTab === 'navy' }" @click="changeTab('navy')">Navy</span>
        </NuxtLink>
        <NuxtLink to="/offer">
          <span :class="{ active: activeTab === 'offer' }" @click="changeTab('offer')">Oferta</span>
        </NuxtLink>
        <NuxtLink to="/contact">
          <span :class="{ active: activeTab === 'contact' }" @click="changeTab('contact')">Kontakt</span>
        </NuxtLink>
        <div class="TheNavbar__icons">
          <a href="#" class="facebook">
            <nuxt-img
              :lazy="true"
              format="webp"
              :src="facebook"
              alt="facebook icon"
            />
          </a>
          <a href="#" class="instagram">
            <nuxt-img
              :lazy="true"
              format="webp"
              :src="instagram"
              alt="instagram icon"
            />
          </a>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import TheLogo from '~/components/TheLogo'
export default {
  name: 'TheNavbar',
  components: {
    TheLogo
  },
  data () {
    return {
      facebook: '/images/facebook.webp',
      instagram: '/images/instagram.webp',
      activeTab: '',
      showMore: false,
      isScrollHidden: false
    }
  },
  mounted () {
    window.addEventListener('scroll', this.handleScroll)
  },
  methods: {
    toggleMenu () {
      this.showMore = !this.showMore
      if (this.showMore) {
        document.body.style.overflow = 'hidden'
      } else {
        document.body.style.overflow = 'auto'
      }
    },
    changeTab (tab) {
      this.activeTab = tab
      this.showMore = false
    },
    handleScroll () {
      if (window.scrollY > 10) {
        this.isScrollHidden = true
      } else {
        this.isScrollHidden = false
      }
    },
    setMenuHeightForMobile () {
      if (typeof window !== 'undefined' && window.innerWidth < 1150) {
        const viewportHeight = window.innerHeight
        const topBarHeight = window.visualViewport.offsetTop
        const menuHeight = viewportHeight - topBarHeight
        return `${menuHeight}px`
      }
      return '100vh'
    }
  }
}
</script>
<style lang="css" scoped>
.TheNavbar {
  width: 100%;
  display: flex;
  color: black;
  position: relative;
  height: 10vh;
  z-index: 2;
}
.TheNavbar__navbar {
  padding: 0 10%;
  transition: 0.5s all ease-in;
  background-color: #F0F0F0;
}
.TheNavbar__navbar-buttons a {
  color: black;
  text-decoration: none;
  position: relative;
}
.TheNavbar__navbar-buttons a::before {
  content: '';
  position: absolute;
  width: 100%;
  height: 1px;
  border-radius: 4px;
  background-color: black;
  bottom: -1px;
  left: 0;
  transform-origin: right;
  transform: scaleX(0);
  transition: transform .2s ease-in-out;
}
.TheNavbar__navbar-buttons a:hover::before {
  transform-origin: left;
  transform: scaleX(1);
}
.TheNavbar__navbar {
  display: flex;
  align-items: center;
  text-transform: uppercase;
  font-size: 0.8rem;
  width: 100%;
  justify-content: space-between;
  gap: 1rem;
}
.TheNavbar__navbar-buttons {
  display: flex;
  gap: 2rem;
}
.TheNavbar__logo {
  filter: invert(1);
}
.TheNavbar__icons{
  display: flex;
  gap: 0.3rem;
}
.TheNavbar__icons img {
  height: 1.2rem
}
.active {
  font-weight: bold;
  cursor: default;
}
.TheNavbar__mobile {
  display: none;
}
.TheNavbar__mobile-content {
  display: none;
}
@media only screen and (max-width: 1150px) {
  .TheNavbar__mobile {
    display: flex;
    justify-content: space-between;
    width: 100%;
    padding: 0 3%;
  }
  .TheNavbar__navbar {
    display: none;
  }
  .TheNavbar__mobile-content {
    background-color: #212121;
    position: absolute;
    height: 100%;
    width: 100%;
    z-index: 10;
    display: block;
    transition: all 0.3s ease-out;
  }
  .TheNavbar__mobile-buttons {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    height: 100%;
    gap: 2rem;
    padding: 0 3rem;
    transition: all 0.3s ease-out;
  }
  .TheNavbar__mobile-buttons a{
    color: white;
    text-decoration: none;
    text-transform: uppercase;
    font-size: 1.2rem;
    text-align: left;
    display: block;
    margin: 0 auto 0 0
  }
  .TheNavbar__menu {
    position: relative;
    display: flex;
    justify-content: center;
    align-items: center;
    width: 2rem;
    height: 2rem;
    cursor: pointer;
    transition: all .5s ease-in-out;
    margin: 1rem;
  }
  .TheNavbar__menu-burger {
    width: 20px;
    height: 2px;
    background: black;
    transition: all .5s ease-in-out;;
  }
  .TheNavbar__menu-burger::before,
  .TheNavbar__menu-burger::after {
    content: '';
    position: absolute;
    width: 20px;
    height: 2px;
    background: black;
    transition: all .5s ease-in-out;;
  }
  .TheNavbar__menu-burger::before {
    transform: translate3d(0, -5px, 0)
  }
  .TheNavbar__menu-burger::after {
    transform: translate3d(0, 5px, 0)
  }
  .TheNavbar__menu.open .TheNavbar__menu-burger {
    transform: translate3d(-20px, 0, 0);
    background: transparent;
    box-shadow: none;
  }
  .TheNavbar__menu.open .TheNavbar__menu-burger::before {
    transform: rotate(45deg) translate3d(14px, -14px, 0);
    background-color: white;
  }
  .TheNavbar__menu.open .TheNavbar__menu-burger::after {
    transform: rotate(-45deg) translate3d(14px, 14px, 0);
    background-color: white;
  }
  .TheNavbar__icons {
    filter: invert(1);
    position: absolute;
    bottom: 3rem;
    right: 2rem;
    gap: 0.5rem;
  }
  .TheNavbar__icons img {
    height: 1.5rem;
  }
}
@media only screen and (max-width: 576px) {
  .TheNavbar__mobile-buttons a{
    font-size: 0.9rem;
  }
}
</style>
