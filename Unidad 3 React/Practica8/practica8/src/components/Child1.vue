<template>
  <div class="child-container">
    <h2>Soy el componente hijo 1 👦🏽</h2>
    <p>{{ number }}</p>
  </div>
</template>

<script>
export default {
  name: 'Child1',
  props: {
    number: {
      type: Number,
      required: true
    }
  }
}
</script>

<style scoped>
.child-container {
  text-align: left;
  margin: 0;
}

h2 {
  font-weight: bold;
  color: white;
  margin: 0 0 1px 0;
}

p {
  font-weight: bold;
  color: white;
  margin: 0;
  font-size: 1.2em;
}
</style>