<template>
  <div class="TheNavbar">
    <navbar class="TheNavbar__navbar">
      <div class="TheNavbar__navbar-buttons">
        <NuxtLink to="/contact">
          Portfolio
        </NuxtLink>
        <NuxtLink to="/contact">
          Navy
        </NuxtLink>
      </div>
      <div class="TheNavbar__logo">
        <TheLogo/>
      </div>
      <div class="TheNavbar__navbar-buttons">
        <NuxtLink to="/services">
          Oferta
        </NuxtLink>
        <NuxtLink to="/contact">
          Kontakt
        </NuxtLink>
      </div>
    </navbar>
  </div>
</template>

<script>
import TheLogo from '~/components/TheLogo'
export default {
  name: 'TheNavbar',
  components: {
    TheLogo
  }
}
</script>
<style lang="css" scoped>
.TheNavbar {
  width: 100%;
  display: flex;
  color: #fefefe;
  position: relative;
}
.TheNavbar a {
  color: #fefefe;
  text-decoration: none;
  position: relative;
}
.TheNavbar a::before {
  content: '';
  position: absolute;
  width: 100%;
  height: 1px;
  border-radius: 4px;
  background-color: #ededed;
  bottom: -1px;
  left: 0;
  transform-origin: right;
  transform: scaleX(0);
  transition: transform .2s ease-in-out;
}
.TheNavbar a:hover::before {
  transform-origin: left;
  transform: scaleX(1);
}
.TheNavbar a:hover {
  color: #ededed;
}
.TheNavbar__navbar {
  display: flex;
  align-items: center;
  text-transform: uppercase;
  font-size: 0.8rem;
  letter-spacing: 1px;
  width: 100%;
  justify-content: space-between;
}
.TheNavbar__navbar-buttons {
  display: flex;
  gap: 5rem;
}
.TheNavbar__logo {
  margin: 0 10rem;
}
</style>
