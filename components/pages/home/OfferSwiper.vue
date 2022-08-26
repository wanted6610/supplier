<template>
  <hooper>
    <slide v-for="(slide, index) in slides" :key="slide.id">
      <h3 class="slide__title">{{slide.title}}</h3>
      <p class="slide__desc">{{slide.desc}}</p>
    </slide>
  </hooper>
</template>

<script>
import { Hooper, Slide } from 'hooper';
import 'hooper/dist/hooper.css';

export default {
  name: "BaseSwiper",
  components: {Hooper, Slide},
  props: {
    slides: {
      type: Array,
      default: () => [],
    }
  }
}
</script>

<style scoped>

</style>
