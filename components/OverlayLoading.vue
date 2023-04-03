<template>
  <div class="loading-overlay">
    <nuxt-img
      :lazy="true"
      format="webp"
      class="loading-logo"
      :src="image"
      alt="logo"
    />
  </div>
</template>

<script>
export default {
  name: 'LoadingOverlay',
  data () {
    return {
      image: '/images/logo.webp'
    }
  }
}
</script>

<style>
.loading-overlay {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  z-index: 9999;
  background-color: black;
  display: flex;
  justify-content: center;
  align-items: center;
}

.loading-logo {
  width: 5rem;
  animation: pulsate 1s ease-in-out infinite;
}

@keyframes pulsate {
  0% {
    transform: scale(1);
  }
  50% {
    transform: scale(1.1);
  }
  100% {
    transform: scale(1);
  }
}
</style>
