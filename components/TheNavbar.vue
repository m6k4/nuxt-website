<template>
  <div class="TheNavbar">
    <TheLogo />
    <navbar class="TheNavbar__navbar">
      <NuxtLink to="/contact">
        About
      </NuxtLink>
      <NuxtLink to="/services">
        Services
      </NuxtLink>
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
  height: 120px;
  width: 100%;
  display: flex;
  padding: 20px 30px;
}

.TheNavbar__navbar {
  margin-left: auto;
  display: flex;
  align-items: center;
  gap: 30px;
}
</style>
