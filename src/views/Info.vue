<template>
    <div>
        <barra></barra>
        <body-info></body-info>
        <pie></pie>
    </div>
</template>

<script>
import Barra from '../components/main/Barra.vue'
import BodyInfo from '../components/main/BodyInfo.vue'
import Pie from '../components/main/Pie.vue'
export default {
  components: { Barra, Pie, BodyInfo },
    methods: {

    }
}
</script>