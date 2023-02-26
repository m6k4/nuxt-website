<template>
  <div class="PorfolioImagesGrid">
    <div class="PorfolioImagesGrid__grid">
      <div class="PorfolioImagesGrid__grid-item-1 PorfolioImagesGrid__image" :style="!isBiggerImageLeft && 'height: 50%;'">
        <ImageTitle :title="'.Nazwa 1'" :content="'wnętrza warszawa'" class="PorfolioImagesGrid__grid-text" />
        <img
          :src="imageFirst"
          :alt="imageFirstDescription"
          class="PorfolioImagesGrid__image"
        >
      </div>
      <div
        v-if="!isBiggerImageLeft"
        class="PorfolioImagesGrid__grid-item-2 PorfolioImagesGrid__image"
        style="height: 50%;"
      >
        <ImageTitle :title="'.Nazwa 2'" :content="'wnętrza warszawa'" class="PorfolioImagesGrid__grid-text" />
        <img
          :src="imageSecond"
          :alt="imageSecondDescription"
          class="PorfolioImagesGrid__image"
        >
      </div>
    </div>
    <div class="PorfolioImagesGrid__grid">
      <div
        v-if="isBiggerImageLeft"
        class="PorfolioImagesGrid__grid-item-2 PorfolioImagesGrid__image"
        style="height: 50%;"
      >
        <ImageTitle :title="'.Nazwa 2'" :content="'wnętrza warszawa'" class="PorfolioImagesGrid__grid-text" />
        <img
          :src="imageSecond"
          :alt="imageSecondDescription"
          class="PorfolioImagesGrid__image"
        >
      </div>
      <div
        class="PorfolioImagesGrid__grid-item-3 PorfolioImagesGrid__image"
        :style="isBiggerImageLeft && 'height: 50%;'"
      >
        <ImageTitle :title="'.Nazwa 3'" :content="'wnętrza warszawa'" class="PorfolioImagesGrid__grid-text" />
        <img
          :src="imageThird"
          :alt="imageThirdDescription"
          class="PorfolioImagesGrid__image"
        >
      </div>
    </div>
  </div>
</template>
<script>
import ImageTitle from '~/components/ImageTitle'
export default {
  name: 'TheContentComPorfolioImagesGridponent',
  components: {
    ImageTitle
  },
  layout: 'page',
  props: ['imageFirst', 'imageFirstDescription', 'imageSecond', 'imageSecondDescription', 'imageThird', 'imageThirdDescription', 'isBiggerImageLeft']
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
.PorfolioImagesGrid__image img:hover{
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
