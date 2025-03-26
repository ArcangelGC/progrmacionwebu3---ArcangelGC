<template>
  <div class="parent-container">
    <h1 class="parent-title">Soy el componente padre 👨🏽</h1>
    <Child1 :number="numberToPass" />
    <Child2 :age="childAge" />
  </div>
</template>

<script>
import Child1 from './Child1.vue'
import Child2 from './Child2.vue'

export default {
  name: 'ParentComponent',
  components: {
    Child1,
    Child2
  },
  data() {
    return {
      numberToPass: 10,
      childAge: 4
    }
  }
}
</script>

<style scoped>
.parent-container {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  gap: 10px;
  padding: 20px;
}

.parent-title {
  font-weight: bold;
  color: white;
  margin: 0 0 15px 0; /* Añadí margen inferior para mejor espaciado */
  font-size: 50px; /* Tamaño exacto que solicitaste */
  letter-spacing: 0.5px; /* Mejor legibilidad */
  line-height: 1.3; /* Espaciado entre líneas */
}
</style>