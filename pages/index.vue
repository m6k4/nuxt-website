<template>
  <div>
    <MainPage class="MainPage" />
  </div>
</template>

<script>
import MainPage from '~/components/MainPage.vue'

export default {
  name: 'IndexPage',
  components: {
    MainPage
  },
  layout: 'page'
}
</script>
<style>
    html {
      background-color: #F0F0F0;
      margin: 0;
      padding: 0;
      width: 100%;
      box-sizing: border-box;
      font-family: 'Montserrat', sans-serif;
      font-size: 16px;
    }
    * {
    box-sizing: inherit;
    }

</style>
