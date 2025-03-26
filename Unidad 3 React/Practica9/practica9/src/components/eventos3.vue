<template>
    <div>
      <h2>Evento Mouse</h2>
      <div 
        @mouseenter="mensajeMostrado = true" 
        @mouseleave="mensajeMostrado = false"
        style="width: 100px; height: 100px; background-color: black; margin: 10px;">
      </div>
      <p v-if="mensajeMostrado" style="margin-top: 10px;">El puntero ha sido guardado.</p>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        mensajeMostrado: false
      };
    }
  }
  </script>