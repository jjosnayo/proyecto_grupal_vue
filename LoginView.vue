<template>
  <div>
    <input type="text" v-bind:value="nombre" v-on:input="verificar_nombre"><br>
    <input type="text" v-bind:value="contrasenha" v-on:input="verificar_contrasenha"><br>
    <button v-on:click="casa">Login</button>
  </div>
  <nav>
    <router-link to="/registrar">Registrarse</router-link>
  </nav>
</template>

<script>
export default {
  name: "LoginView",
  data(){
    return{
      nombre: "",
      contrasenha: ""
    }
  },
  methods: {
    casa(){
      this.$router.push('/home')
    },
    verificar_nombre(e){
      this.nombre = e.target.value
    },
    verificar_contrasenha(e){
      this.contrasenha = e.target.value
    }
  }
}
</script>

<style scoped>

</style>