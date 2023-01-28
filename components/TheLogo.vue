<template>
  <img
    class="TheLogo"
    :src="image"
    alt="logo"
  >
</template>

<script>
export default {
  name: 'TheLogo',
  data () {
    return {
      image: 'images/logo.png'
    }
  }
}
</script>
<style lang="css" scoped>
.TheLogo {
    width: 8rem;
    height: auto;
  }
</style>
