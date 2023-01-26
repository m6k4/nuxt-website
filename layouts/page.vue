<template>
  <div>
    <TheNavbar />
    <Nuxt />
    <TheFooter />
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
