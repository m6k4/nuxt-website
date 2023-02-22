<template>
  <div class="GoogleMap">
    <div class="GoogleMap__canvas">
      <iframe
        id="GoogleMap__canvas"
        width="100%"
        height="100%"
        src="https://maps.google.com/maps?q=ul.%20Konstruktorska%2010C/31%2002-673%20Warszawa&t=&z=13&ie=UTF8&iwloc=&output=embed"
        frameborder="0"
        scrolling="no"
        marginheight="0"
        marginwidth="0"
      />
    </div>
  </div>
</template>
<script>
export default {
  name: 'GoogleMap',
  data () {
    return {}
  }

}
</script>
<style lang="css" scoped>
.GoogleMap {
  width: 100%;
  height: 100%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  text-transform: none;
}

.GoogleMap__canvas {
  width: 100%;
  height: 100%;
  overflow: hidden;
  background: none !important;
}
</style>
