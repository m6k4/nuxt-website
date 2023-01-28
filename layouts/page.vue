<template>
  <div>
    <TheNavbar />
    <Nuxt />
    <TheFooter />
    <!-- <MainPage /> -->
  </div>
</template>
<script>
import TheNavbar from '~/components/TheNavbar'
import TheFooter from '~/components/TheFooter'
// import MainPage from '~/components/MainPage.vue'

export default {
  name: 'ThePage',
  components: {
    TheNavbar, TheFooter
  }
}
</script>
