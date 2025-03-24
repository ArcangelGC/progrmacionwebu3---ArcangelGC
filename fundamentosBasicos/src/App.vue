<template>
  <div id="app">
    <h1 class="title">Gatos</h1>
    <div class="cards-container">
      <Practica5 
        title="Gato Negro" 
        body="Los gatos negros son conocidos por su elegancia y misterio. A menudo se asocian con la buena suerte en algunas culturas, mientras que en otras se les considera un símbolo de mala suerte. Sin embargo, son tan cariñosos y juguetones como cualquier otro gato."
      />
      <Practica5 
        title="Gato Naranja" 
        body="Los gatos naranjas, también conocidos como gatos atigrados naranjas, son famosos por su personalidad amigable y extrovertida. Suelen ser muy sociables y les encanta estar cerca de las personas. Además, su pelaje brillante los hace muy llamativos."
      />
    </div>
  </div>
</template>

<script>
import HelloWorld from './HelloWorld.vue';

export default {
  name: 'App',
  components: {
    HelloWorld
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  text-align: center;
  margin-top: 60px;
}

.title {
  font-size: 2.5rem;
  margin-bottom: 20px;
}

.cards-container {
  display: flex;
  justify-content: center;
  gap: 20px;
  flex-wrap: wrap;
}
</style>