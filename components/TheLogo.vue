<template>
  <NuxtLink to="/">
    <img
      class="TheLogo"
      :src="image"
      alt="logo"
    >
  </NuxtLink>
</template>

<script>
export default {
  name: 'TheLogo',
  data () {
    return {
      image: '/images/logo.png'
    }
  }
}
</script>
<style lang="css" scoped>
.TheLogo {
    width: 5rem;
    height: auto;
  }
</style>
