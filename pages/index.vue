<template>
  <div>
    <TheBackground />
  </div>
</template>

<script>
import TheBackground from '~/components/TheBackground'
export default {
  name: 'IndexPage',
  components: {
    TheBackground
  },
  layout: 'page'
}
</script>
<style>
    html {
      margin: 0;
      padding: 0;
      width: 100%;
      height: 100vh;
      box-sizing: border-box;
      font-family: 'Montserrat', sans-serif;
      font-size: 16px;
      overflow: hidden;
    }
    body {
      padding: 0 10%;
    }
    * {
    box-sizing: inherit;
    }

</style>
