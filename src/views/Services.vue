<template>
    <div>
        <barra></barra>
        <body-services></body-services>
        <pie></pie>
    </div>
</template>

<script>
import Barra from '../components/main/Barra.vue'
import BodyServices from '../components/main/BodyServices.vue'
import Pie from '../components/main/Pie.vue'
export default {
  components: { Barra, Pie, BodyServices },
    methods: {

    }
}
</script>