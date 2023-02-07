<template>
    <div class="TheContentComponent">
        <img
        :src="mainImage"
        alt="kids_room"
        class="TheContentComponent__image"
        >
      <h1 class="TheContentComponent__title">{{ title }}</h1>
      <div class="TheContentComponent__content">
        {{ content }}
      </div>
    </div>
  </template>
<script>
export default {
  name: 'TheContentComponent',
  props: ['title', 'content', 'mainImage'],
  layout: 'page'
}
</script>
<style lang="css" scoped>
.TheContentComponent{
  height: 90vh;
  padding: 0 10%;
  position: relative;
}
.TheContentComponent__image{
  height: 100%;
}
.TheContentComponent__title{
  font-family: 'Playfair Display', serif;
  color: black;
  position: absolute;
  top: 15%;
  left: 45%;
  text-transform: uppercase;
  font-size: 4.5vw;
  line-height: 1rem;
  font-weight: 400;
}
.TheContentComponent__content {
  position: absolute;
  bottom: 20%;
  font-size: 0.8rem;
  width: 40%;
  right: 10%;
  font-weight: 500;
  text-transform: uppercase;
}
@media only screen and (max-width: 1600px) {
  .TheContentComponent__content {
    font-size: 0.6rem;
  }
}
</style>
