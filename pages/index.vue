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
      height: 100%;
      box-sizing: border-box;
      font-family: 'Montserrat', sans-serif;
      font-size: 16px;
    }
    body {
      padding: 0 20rem;
    }
    * {
    box-sizing: inherit;
    }
    @media only screen and (max-width: 1600px) {
    body {
      padding: 0 10rem;
    }
}
</style>
