<template>
  <div>
    <input type="text" v-bind:value="nombre_producto" v-on:input="registrar_nproducto"><br>
    <input type="text" v-bind:value="tipo_producto" v-on:input="registrar_tproducto"><br>
    <button v-on:click="productos">Registrar producto</button>
  </div>
</template>

<script>
export default {
  name: "RegistrarProductoView",
  data(){
    return {
      nombre_producto: "",
      tipo_producto: ""
    }
  },
  methods: {
    productos(){
      this.$router.push('/ventas')
    },
    registrar_nproducto(e){
      this.nombre_producto = e.target.value
    },
    registrar_tproducto(e){
      this.tipo_producto = e.target.value
    }
  }
}
</script>

<style scoped>

</style>