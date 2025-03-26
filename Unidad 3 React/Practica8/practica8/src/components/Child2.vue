<template>
  <div class="child-container">
    <h2>Soy el componente hijo 2 👦🏽</h2>
    <p>{{ age }}</p>
  </div>
</template>

<script>
export default {
  name: 'Child2',
  props: {
    age: {
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
  color: rgb(255, 255, 255);
  margin: 0 0 1px 0;
}

p {
  font-weight: bold;
  color: white;
  margin: 0;
  font-size: 1.2em;
}
</style>