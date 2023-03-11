<template>
  <div class="PorfolioImagesGrid">
    <div class="PorfolioImagesGrid__grid">
      <NuxtLink
        :to="linkFirst.link"
        class="PorfolioImagesGrid__grid-item-1 PorfolioImagesGrid__image"
        :style="!isBiggerImageLeft && 'height: 50%;'"
      >
        <ImageTitle
          class="PorfolioImagesGrid__grid-text"
          :title="linkFirst.title"
          :content="linkFirst.subtitle"
        />
        <div class="PorfolioImagesGrid__image-container">
          <img
            loading="lazy"
            :src="linkFirst.image"
            :alt="linkFirst.description"
            class="PorfolioImagesGrid__image"
          >
        </div>
      </NuxtLink>
      <NuxtLink
        v-if="!isBiggerImageLeft"
        :to="linkSecond.link"
        class="PorfolioImagesGrid__grid-item-2 PorfolioImagesGrid__image"
        style="height: 50%;"
      >
        <ImageTitle
          class="PorfolioImagesGrid__grid-text"
          :title="linkSecond.title"
          :content="linkSecond.subtitle"
        />
        <div class="PorfolioImagesGrid__image-container">
          <img
            loading="lazy"
            :src="linkSecond.image"
            :alt="linkSecond.description"
            class="PorfolioImagesGrid__image"
          >
        </div>
      </NuxtLink>
    </div>
    <div class="PorfolioImagesGrid__grid">
      <NuxtLink
        v-if="isBiggerImageLeft"
        :to="linkSecond.link"
        class="PorfolioImagesGrid__grid-item-2 PorfolioImagesGrid__image"
        style="height: 50%;"
      >
        <ImageTitle
          class="PorfolioImagesGrid__grid-text"
          :title="linkSecond.title"
          :content="linkSecond.subtitle"
        />
        <div class="PorfolioImagesGrid__image-container">
          <img
            loading="lazy"
            :src="linkSecond.image"
            :alt="linkSecond.description"
            class="PorfolioImagesGrid__image"
          >
        </div>
      </NuxtLink>
      <NuxtLink
        :to="linkThird.link"
        class="PorfolioImagesGrid__grid-item-3 PorfolioImagesGrid__image"
        :style="isBiggerImageLeft && 'height: 50%;'"
      >
        <ImageTitle
          class="PorfolioImagesGrid__grid-text"
          :title="linkThird.title"
          :content="linkThird.subtitle"
        />
        <div class="PorfolioImagesGrid__image-container">
          <img
            loading="lazy"
            :src="linkThird.image"
            :alt="linkThird.description"
            class="PorfolioImagesGrid__image"
          >
        </div>
      </NuxtLink>
    </div>
  </div>
</template>
<script>
import ImageTitle from '~/components/ImageTitle'
export default {
  name: 'PorfolioImagesGrid',
  components: {
    ImageTitle
  },
  layout: 'page',
  props: {
    linkFirst: {
      type: Object,
      required: true
    },
    linkSecond: {
      type: Object,
      required: true
    },
    linkThird: {
      type: Object,
      required: true
    },
    isBiggerImageLeft: {
      type: Boolean,
      required: true
    }
  }
}
</script>
<style lang="css" scoped>
.PorfolioImagesGrid{
  width: 100%;
  display: flex;
}
.PorfolioImagesGrid__grid{
  width: 50%;
  height: 130vh;
  display: flex;
  flex-direction: column;
  position: relative;
}
.PorfolioImagesGrid__grid img{
  transition: all 0.3s ease-in-out;
  width: 110%;
}
.PorfolioImagesGrid__image {
  height: 100%;
  overflow: hidden;
  position: relative;
  cursor: pointer;
}
.PorfolioImagesGrid__image img{
  height: 101%;
  object-fit: cover;
}
.PorfolioImagesGrid__image-container {
  height: 101%;
  object-fit: cover;
  transition: filter 0.3s ease;
}
.PorfolioImagesGrid__image-container:hover{
  filter: brightness(70%);
}
.PorfolioImagesGrid__grid-item-1 img {
  transform: translate3d(-5%, 0, 0);
}
.PorfolioImagesGrid__grid-item-3 .PorfolioImagesGrid__grid-item-2 img {
  transform: translate3d(0, 0, 0);
}
.PorfolioImagesGrid__grid-item-3 img:hover{
  transform: translate3d(-5%, 0, 0);
}
.PorfolioImagesGrid__grid-item-2 img:hover {
  transform: translate3d(-5%, 0, 0);
}
.PorfolioImagesGrid__grid-item-1 img:hover {
  transform: translate3d(0, 0, 0);
}
.PorfolioImagesGrid__grid-text {
  left: 0;
  right: 0;
  opacity: 0;
  top: 50%;
  transform: translate3d(0, -50%, 0);
  position: absolute;
  transition: all 0.3s ease-in-out;
  pointer-events: none;
}
.PorfolioImagesGrid__grid-item-1:hover .PorfolioImagesGrid__grid-text {
  opacity: 1;
}
.PorfolioImagesGrid__grid-item-2:hover .PorfolioImagesGrid__grid-text {
  opacity: 1;
}
.PorfolioImagesGrid__grid-item-3:hover .PorfolioImagesGrid__grid-text {
  opacity: 1;
}
@media only screen and (max-width: 1280px) {
  .PorfolioImagesGrid__grid{
    height: 100vh;
  }
}
@media only screen and (max-width: 1000px) {
  .PorfolioImagesGrid__grid{
    height: 80vh;
  }
}
@media only screen and (max-width: 750px) {
  .PorfolioImagesGrid__grid{
    height: 60vh;
  }
}
@media only screen and (max-width: 576px) {
  .PorfolioImagesGrid{
    flex-direction: column;
  }
  .PorfolioImagesGrid__grid {
    width: 100%
  }
  .PorfolioImagesGrid__grid-text {
    opacity: 1;
  }
  .PorfolioImagesGrid__image {
    height: 50%;
  }
  .PorfolioImagesGrid__grid{
    height: auto;
  }
}
</style>
