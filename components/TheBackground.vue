<template>
  <div class="TheBackground">
    <!-- <img
      class="TheBackground__img"
      :src="image"
      alt="bedroom"
    > -->
  </div>
</template>

<script>
export default {
  name: 'TheBackground',
  data () {
    return {
      image: 'images/bedroom-1.jpeg'
    }
  }
}
</script>
<style lang="css" scoped>
.TheBackground {
  background-color: #212121;
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  z-index: -1;
}

.TheBackground__img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}
</style>
