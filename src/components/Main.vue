<script>
import Title from './sections/Title.vue'
import Abstract from './sections/Abstract.vue'
import BibTeX from './sections/BibTeX.vue'
import Carousel from './sections/Carousel.vue'
import Overview from './sections/Overview.vue'
import Bench from './sections/Bench.vue'
import MazeVariations from './sections/MazeVariations.vue'
import ImageSlider from './sections/ImageSlider.vue'
import ImageSliderInner from './sections/ImageSliderInner.vue'
import ImageSelector from './sections/ImageSelector.vue'
import Table from './sections/Table.vue'
import SeletionForComparison from './sections/SeletionForComparison.vue'
import Model3D from './sections/Model3D.vue'
import GaussianSplats3D from './sections/GaussianSplats3D.vue'

export default {
  components: {
    Title,
    Abstract,
    BibTeX,
    Carousel,
    Overview,
    Bench,
    MazeVariations,
    ImageSlider,
    ImageSliderInner,
    ImageSelector,
    Table,
    SeletionForComparison,
    Model3D,
    GaussianSplats3D
  }
}
</script>

<template>
  <Title/>
  <Carousel/>
  <Overview/>
  <Abstract/>
  <Table/>
  <Bench/>
  <MazeVariations/>
  <Model3D/>
  <GaussianSplats3D/>
  <SeletionForComparison/>
  <ImageSliderInner/>
  <ImageSlider/>
  <ImageSelector/>
  <BibTeX/>
</template>
