<template>
  <div class="ThePage">
    <TheNavbar class="TheNavbar"/>
    <Nuxt />
    <TheFooter class="TheFooter"/>
  </div>
</template>
<script>
import TheNavbar from '~/components/TheNavbar'
import TheFooter from '~/components/TheFooter'

export default {
  name: 'ThePage',
  components: {
    TheNavbar, TheFooter
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
  position: fixed;
  bottom: 0;
  width: 100%;
  height: 3rem;
}
</style>
