<template>
  <div class="ThePage">
    <TheNavbar class="TheNavbar"/>
    <Nuxt />
    <MainPage class="MainPage"/>
    <TheFooter class="TheFooter"/>
  </div>
</template>
<script>
import TheNavbar from '~/components/TheNavbar'
import TheFooter from '~/components/TheFooter'
import MainPage from '~/components/MainPage.vue'

export default {
  name: 'ThePage',
  components: {
    TheNavbar, TheFooter, MainPage
  }
}
</script>
<style lang="css" scoped>
.ThePage {
  position: relative;
}
.TheFooter {
  position: sticky;
  bottom: 0;
}
</style>
