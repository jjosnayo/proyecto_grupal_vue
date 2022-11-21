<template>
  <div>
    <h1>Esta es la página de ventas</h1>
    <table>
      <tr>
        <th>Nombre</th>
        <th>Tipo</th>
      </tr>
      <tr v-for="producto of productos" v-bind:key="producto">
        <td>{{producto.nombre_producto}}</td>
        <td>{{producto.tipo_producto}}</td>
      </tr>
    </table>
  </div>
  <nav>
    <router-link to="/registrar_producto">Registrar producto</router-link> |
    <router-link to="/home">Casa</router-link>
  </nav>
</template>

<script>
export default {
  name: "VentasView",
  data(){
    return{
      productos: [
        {nombre_producto: "oreo", tipo_producto: "galleta"},
        {nombre_producto: "coca cola", tipo_producto: "gaseosa"},
        {nombre_producto: "sublime", tipo_producto: "chocolate"}
      ]
    }
  }
}
</script>

<style scoped>
table{
  padding-left: 575px;
}
</style>