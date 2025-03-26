<template>
  <div id="app">
    <div class="background-image"></div>
    <ParentComponent />
  </div>
</template>

<script>
import ParentComponent from './components/ParentComponent.vue'

export default {
  name: 'App',
  components: {
    ParentComponent
  }
}
</script>

<style>
/* Estilos para el fondo */
body, html {
  margin: 0;
  padding: 0;
  height: 100%;
}

.background-image {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-image: url('https://img.freepik.com/vector-gratis/fondo-lineas-dinamicas-estilo-papel_23-2149008629.jpg');
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  z-index: -1; /* Para que quede detrás del contenido */
  opacity: 0.9; /* Ajusta la opacidad si es necesario */
}

#app {
  position: relative;
  z-index: 1;
  min-height: 100vh;
  padding: 20px;
}
</style>