<template>
  <div>
    <barra-supp></barra-supp>
  </div>
</template>

<script>
import swal from 'sweetalert';
import BarraSupp from '../../components/userFE/BarraSupp.vue';
export default {
  components: { BarraSupp },
  name: 'User',
  data (){
    return {
      drawer: true,
    }
  }
};
</script>