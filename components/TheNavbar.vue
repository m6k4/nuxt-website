<template>
  <div class="TheNavbar">
    <div class="TheNavbar__navbar">
      <div class="TheNavbar__logo">
        <TheLogo />
      </div>
      <div class="TheNavbar__navbar-buttons">
        <NuxtLink to="/portfolio" >
          <span @click="activeTab = 'portfolio'" :class="{ active: activeTab === 'portfolio' }">Portfolio</span>
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
        <a href="#" class="facebook">
          <img :src="facebook">
        </a>
        <a href="#" class="instagram">
          <img :src="instagram">
        </a>
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
      facebook: 'images/facebook.png',
      instagram: 'images/instagram.png',
      activeTab: ''
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
  padding: 0 10%;
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
</style>
