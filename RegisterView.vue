<template>
  <div>
    <input type="text" v-bind:value="nombre" v-on:input="registrar_nombre"><br>
    <input type="text" v-bind:value="contrasenha" v-on:input="registrar_contrasenha"><br>
    <button v-on:click="casa">Registrar</button>
  </div>
</template>

<script>
export default {
  name: "RegisterView",
  data(){
    return {
      nombre: "",
      contrasenha: ""
    }
  },
  methods: {
    casa(){
      this.$router.push('/home')
    },
    registrar_nombre(e){
      this.nombre = e.target.value
    },
    registrar_contrasenha(e){
      this.contrasenha = e.target.value
    }
  }
}
</script>

<style scoped>

</style>