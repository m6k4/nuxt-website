<template>
  <div class="Portfolio">
    <TheContentComponent :title="title" :content="content" :main-image="kidsRoom" :is-scrollable="true" />
    <div class="Portfolio__image-grids">
      <PorfolioImagesGrid
        :link-first="portfolioLinks.pulpchair"
        :link-second="portfolioLinks.t_house"
        :link-third="portfolioLinks.layla"
        :is-bigger-image-left="false"
      />
      <PorfolioImagesGrid
        :link-first="portfolioLinks.crystal_port_praski"
        :link-second="portfolioLinks.ost"
        :link-third="portfolioLinks.klobucka"
        :is-bigger-image-left="true"
      />
      <PorfolioImagesGrid
        :link-first="portfolioLinks.two_side"
        :link-second="portfolioLinks.sarmacka"
        :link-third="portfolioLinks.forest_room"
        :is-bigger-image-left="false"
      />
      <PorfolioImagesGrid
        :link-first="portfolioLinks.minska"
        :link-second="portfolioLinks.aroma_park"
        :link-third="portfolioLinks.ursus"
        :is-bigger-image-left="true"
      />
    </div>
  </div>
</template>
<script>
import TheContentComponent from '~/components/TheContentComponent'
import PorfolioImagesGrid from '~/components/PorfolioImagesGrid'
import { portfolioLinks } from '~/data/portfolio'
export default {
  name: 'PortfolioPage',
  components: {
    TheContentComponent,
    PorfolioImagesGrid
  },
  layout: 'page',
  data () {
    return {
      portfolioLinks,
      kidsRoom: '/images/portfolio/kids_room.jpg',
      title: 'Portfolio.',
      content: 'Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industrys standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries.'
    }
  }
}
</script>
<style lang="css" scoped>
.Portfolio__image-grids{
  margin-top: 80px
}
</style>
