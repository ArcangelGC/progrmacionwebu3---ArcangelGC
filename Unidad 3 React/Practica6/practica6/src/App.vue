<script setup>
import barra from './components/barra.vue';
import card from './components/card.vue';
import formulario from './components/formulario.vue';
import carrusel from './components/carrusel.vue';
import HelloWorld from './components/HelloWorld.vue'
</script>

<template>
<barra/>
<card/>
<formulario/>
<carrusel/>

</template>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
