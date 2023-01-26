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
    width: 180px;
    height: auto;
  }
</style>
