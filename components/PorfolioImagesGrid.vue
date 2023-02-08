<template>
  <div class="PorfolioImagesGrid">
      <div class="PorfolioImagesGrid__grid">
      <div class="PorfolioImagesGrid__grid-item-1 PorfolioImagesGrid__image" :style="!isBiggerImageLeft && 'height: 50%;'">
        <!-- <ImageTitle :title="'Nazwa 1'" :content="'wnętrza warszawa'" class="PorfolioImagesGrid__grid-text"/> -->
        <img
          :src="imageFirst"
          :alt="imageFirstDescription"
          class="PorfolioImagesGrid__image"
        >
      </div>
      <div v-if="!isBiggerImageLeft"
      class="PorfolioImagesGrid__grid-item-2 PorfolioImagesGrid__image"
       style="height: 50%;">
        <img
          :src="imageSecond"
          :alt="imageSecondDescription"
          class="PorfolioImagesGrid__image"
        >
      </div>
    </div>
    <div class="PorfolioImagesGrid__grid">
      <div v-if="isBiggerImageLeft"
       class="PorfolioImagesGrid__grid-item-2 PorfolioImagesGrid__image"
       style="height: 50%;">
        <img
          :src="imageSecond"
          :alt="imageSecondDescription"
          class="PorfolioImagesGrid__image"
        >
      </div>
      <div class="PorfolioImagesGrid__grid-item-3 PorfolioImagesGrid__image"
       :style="isBiggerImageLeft && 'height: 50%;'">
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
// import ImageTitle from '~/components/ImageTitle'
export default {
  name: 'TheContentComPorfolioImagesGridponent',
  props: ['imageFirst', 'imageFirstDescription', 'imageSecond', 'imageSecondDescription', 'imageThird', 'imageThirdDescription', 'isBiggerImageLeft'],
  layout: 'page'
  // components: {
  //   ImageTitle
  // }
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
  overflow: hidden
}
.PorfolioImagesGrid__image img{
  height: 101%;
  object-fit: cover;
}
.PorfolioImagesGrid__image img:hover{
  filter: brightness(70%);
}
.PorfolioImagesGrid__grid-item-1 img {
  transform: translateX(-5%);
}
.PorfolioImagesGrid__grid-item-1 img:hover {
  transform: translateX(0);
}
/* .PorfolioImagesGrid__grid-text {
  opacity: 0;
}
.PorfolioImagesGrid__grid:hover .PorfolioImagesGrid__grid-text {
  opacity: 1;
} */
.PorfolioImagesGrid__grid-item-3 .PorfolioImagesGrid__grid-item-2 img {
  transform: translateX(0);
}
.PorfolioImagesGrid__grid-item-3 img:hover{
  transform: translateX(-5%);
}
.PorfolioImagesGrid__grid-item-2 img:hover {
  transform: translateX(-5%);
}
</style>
