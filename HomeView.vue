<template>
  <div class="home">
    <h1>"Bienvenido a Utec Shop"</h1>
    <h2>usuario: {{nombre}}</h2>
    <h2>contraseña: {{contrasenha}}</h2>
  </div>
  <nav>
    <router-link to="/compras">Comprar</router-link> |
    <router-link to="/ventas">Vender</router-link> <br>
    <router-link to="/">Logout</router-link>
  </nav>
</template>

<script>
// @ is an alias to /src
export default {
  name: 'HomeView',
  data(){
    return{
      nombre: "joaquin",
      contrasenha: "10588"
    }
  }
}
</script>
