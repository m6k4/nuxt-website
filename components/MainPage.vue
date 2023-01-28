<template>
    <div class="MainPage">
        <div class="MainPage__content">
            <p>space.</p>
            <p>light.</p>
            <p>proportion.</p>
        </div>
        <img
        class="MainPage__image"
        :src="image"
        alt="living_room"
        >
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
    display: flex;
    justify-content: space-between;
    margin-top: 4rem;
}
.MainPage__content {
    color: #fefefe;
    text-transform: uppercase;
    font-size: 6rem;
    font-weight: 500;
    letter-spacing: -3px;
    line-height: 0;
    font-family: 'Abel', sans-serif;
    align-content: start;
}
.MainPage__image {
    width: 30rem;
}
</style>
