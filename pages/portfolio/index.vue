<template>
  <div class="Portfolio">
    <TheContentComponent :title="title" :content="content" :main-image="kidsRoom" :isScrollable="true" />
    <div class="Portfolio__image-grids">
      <PorfolioImagesGrid :image-first="sinks" :image-second="kidsRoom" :image-third="bathroom" :is-bigger-image-left="false" />
      <PorfolioImagesGrid :image-first="kitchen" :image-second="sink" :image-third="tv" :is-bigger-image-left="true" />
      <PorfolioImagesGrid :image-first="bedroom" :image-second="whiteSink" :image-third="kidsRoomGreen" :is-bigger-image-left="false" />
      <PorfolioImagesGrid :image-first="circleMirror" :image-second="greySofa" :image-third="yellowSofa" :is-bigger-image-left="true" />
    </div>
  </div>
</template>
<script>
import TheContentComponent from '~/components/TheContentComponent'
import PorfolioImagesGrid from '~/components/PorfolioImagesGrid'
export default {
  name: 'PortfolioPage',
  components: {
    TheContentComponent,
    PorfolioImagesGrid
  },
  layout: 'page',
  data () {
    return {
      kidsRoom: 'images/portfolio/kids_room.jpg',
      title: 'Portfolio.',
      content: 'Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industrys standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries.',
      bathroom: 'images/portfolio/bathroom.jpg',
      sink: 'images/portfolio/sink.jpg',
      sinks: 'images/portfolio/sinks.jpg',
      tv: 'images/portfolio/tv.jpg',
      kitchen: 'images/main.jpeg',
      bedroom: 'images/portfolio/bedroom.jpg',
      whiteSink: 'images/portfolio/white_sink.jpg',
      kidsRoomGreen: 'images/portfolio/kidsroom2.jpg',
      circleMirror: 'images/portfolio/circle_mirror.jpg',
      greySofa: 'images/portfolio/grey_sofa.jpg',
      yellowSofa: 'images/portfolio/yellow_sofa.jpg'
    }
  }
}
</script>
<style lang="css" scoped>
.Portfolio__image-grids{
  margin-top: 80px
}
</style>
