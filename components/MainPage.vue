<template>
    <div class="MainPage">
      <img
        :src="image"
        alt="living_room"
        >
      <div class="MainPage__title">
        <p>przestrzen.</p>
        <p>swiatlo.</p>
        <p>proporcja.</p>
      </div>
      <div class="MainPage__content">
        Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries.
      </div>
    </div>
</template>
<script>
export default {
  name: 'MainPage',
  data () {
    return {
      image: 'images/main.jpeg'
    }
  }
}
</script>
<style lang="css" scoped>
.MainPage {
  height: 100vh;
  width: 100%;
  justify-content: center;
  align-items: center;
  position: relative;
}
.MainPage img {
  height: 90%;
  display: block;
  margin: 2rem auto 0 auto;
}
.MainPage__title {
  font-family: 'Playfair Display', serif;
  color: black;
  position: absolute;
  top: 2rem;
  left: 8rem;
  text-transform: uppercase;
  font-size: 4.5vw;
  line-height: 1rem
}
.MainPage__content {
  position: absolute;
  bottom: 15rem;
  font-size: 0.8rem;
  width: 40%;
  right: 5rem;
  font-weight: 500;
  text-transform: uppercase;
}
@media only screen and (max-width: 1600px) {
  .MainPage__content {
    font-size: 0.6rem;
  }
}
</style>
