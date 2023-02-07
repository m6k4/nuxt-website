<template>
    <div class="Portfolio">
      <TheContentComponent :title="title" :content="content" :mainImage="kidsRoom"/>
        <div class="Portfolio__image-grids">
        <PorfolioImagesGrid :imageFirst="sinks" :imageSecond="kidsRoom" :imageThird="bathroom" :isBiggerImageLeft="false"/>
        <PorfolioImagesGrid :imageFirst="kitchen" :imageSecond="sink" :imageThird="tv" :isBiggerImageLeft="true"/>
        <PorfolioImagesGrid :imageFirst="bedroom" :imageSecond="whiteSink" :imageThird="kidsRoomGreen" :isBiggerImageLeft="false"/>
        <PorfolioImagesGrid :imageFirst="circleMirror" :imageSecond="greySofa" :imageThird="yellowSofa" :isBiggerImageLeft="true"/>
    </div>
    </div>
  </template>
<script>
import TheContentComponent from '~/components/TheContentComponent'
import PorfolioImagesGrid from '~/components/PorfolioImagesGrid'
export default {
  name: 'PortfolioPage',
  layout: 'page',
  components: {
    TheContentComponent,
    PorfolioImagesGrid
  },
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
  margin-top: 5rem
}
</style>
