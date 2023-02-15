<template>
    <div class="ImageTitile">
        <p class="ImageTitle__title">{{ title }}</p>
        <p class="ImageTitle__content">{{ content }}</p>
    </div>
  </template>

<script>
export default {
  name: 'ImageTitle',
  props: ['title', 'content']
}
</script>
  <style lang="css" scoped>
  .ImageTitile {
    text-transform: uppercase;
    position: absolute;
    z-index: 1;
    text-align: center;
    opacity: 0;
  }
  .ImageTitle__title {
    color: white;
    font-size: 2.5rem;
    font-family: 'Playfair Display', serif;
    margin: 0 auto;
    line-height: 2rem;
  }
  .ImageTitle__content {
    font-size: 0.9rem;
  }
  @media only screen and (max-width: 1000px) {
  .ImageTitle__title{
    font-size: 2.1rem
  }
  .ImageTitle__content{
    font-size: 0.8rem
  }
}
  @media only screen and (max-width: 750px) {
    .ImageTitle__title{
    font-size: 1.8rem
  }
  .ImageTitle__content{
    font-size: 0.7rem
  }
}

  </style>
