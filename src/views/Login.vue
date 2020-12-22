<template>
    <div id="login" class="login" style="height:39.05rem;">
      <div class="container-fluid">
        <v-btn id="boton-volver" color="#FFCA28" class="mt-3" elevation="6" @click.prevent="volver">
          Volver
        </v-btn>
      </div>
      <div class="row justify-content-center text-center ml-0 mr-0 pt-5">
        <v-card style="width:30rem;" elevation="2">
          <div class="container-fluid mb-3 mt-3">
            <img src="@/static/icon/icon_picto.svg" alt="logo" style="width:18rem;">
          </div>
          <h1>!Bienvenido a Mobi¡</h1>
          <the-login></the-login>
        </v-card>
      </div>
    </div>
</template>

<script>
import TheLogin from '../components/auth/TheLogin.vue'
export default {
  components: { TheLogin },
  methods: {
    async volver(){
      this.$router.push('/')
    }
  }
    
}
</script>
<style scoped>
#login {
  background-image: url(https://www.miescuelafacil.com/web/wp-content/uploads/2017/05/Aumenta-n%C3%BAmero-de-usuario-de-Internet-en-el-mundo.jpg);
  background-size: cover;

}

</style>