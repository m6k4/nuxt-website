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
    font-size: 3rem;
    font-family: 'Playfair Display', serif;
    margin-bottom: 0;
    line-height: 2rem;
  }
  .ImageTitle__content {

  }
  </style>
