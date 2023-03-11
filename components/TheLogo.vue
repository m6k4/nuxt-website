<template>
  <NuxtLink to="/">
    <nuxt-img
      :lazy="true"
      format="webp"
      class="TheLogo"
      :src="image"
      alt="logo"
    />
  </NuxtLink>
</template>

<script>
export default {
  name: 'TheLogo',
  data () {
    return {
      image: '/images/logo.webp'
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
