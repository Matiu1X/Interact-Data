<template>
    <div>
        <barra></barra>
        <carousel></carousel>
        <body-home></body-home>
        <pie></pie>
    </div>
</template>

<script>
import Barra from '../components/main/Barra.vue'
import BodyHome from '../components/main/BodyHome.vue'
import Carousel from '../components/main/Carousel.vue'
import Pie from '../components/main/Pie.vue'
export default {
  components: { Barra, Carousel, Pie, BodyHome },
    methods: {

    }
}
</script>