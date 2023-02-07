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
}
.TheFooter {
  position: sticky;
  bottom: 0;
}
</style>
