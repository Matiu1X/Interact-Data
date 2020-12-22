<template>
  <div>
    
    <v-navigation-drawer
      v-model="drawer"
      :clipped="$vuetify.breakpoint.lgAndUp"
      app
    >
        <v-list>
          <v-list-item-group
          v-model="group"
          active-class="deep-purple--text text--accent-4"
          >
            <v-list-item>
              <v-list-item-title @click="ir_a_Sitio('/')">Inicio</v-list-item-title>
            </v-list-item>
            <v-list-item>
              <v-list-item-title @click="ir_a_Sitio('/info')">Información</v-list-item-title>
            </v-list-item>
            <v-list-item>
              <v-list-item-title @click="ir_a_Sitio('/services')">Servicios</v-list-item-title>
            </v-list-item>
            <v-list-item>
              <v-list-item-title @click="ir_a_Sitio('/login')">Login</v-list-item-title>
            </v-list-item>
          </v-list-item-group>
        </v-list>
    </v-navigation-drawer>
    <v-app-bar dense="true"
    :clipped-left="$vuetify.breakpoint.lgAndUp"
      app>
      <v-toolbar-title>
      <v-app-bar-nav-icon color="#92D1C3" @click.stop="drawer = !drawer"></v-app-bar-nav-icon>
      <span class="ml-3" font-family="Ubuntu">Interact-Data</span>
      </v-toolbar-title>
      <v-spacer></v-spacer>
        <v-btn color="#92D1C3" elevation="2" outlined="true" rounded="true" @click="ir_a_Sitio('/login')">
          Login
        </v-btn>
    </v-app-bar>
  </div>
</template>
<script>
export default {
    name: 'barraSup',
     data(){
        return{
            drawer: false,
        }
    },
    methods:{
        getUserDetails(){
            let user = localStorage.getItem('user');
            let token = localStorage.getItem('jwt');
            if(token){
                this.user = JSON.parse(user)
            }
        },
        logOut(){
            localStorage.removeItem('jwt');
            localStorage.removeItem('user');
            this.$router.push('/');
        },
        async ir_a_Sitio(sitio){
            this.$router.push(sitio)
        }
    },
    created(){
        this.getUserDetails();
    }
}
</script>
<style scoped>
  #login{
    background-color: #42b983;
  }
  #redText{
      color: crimson;
  }
</style>