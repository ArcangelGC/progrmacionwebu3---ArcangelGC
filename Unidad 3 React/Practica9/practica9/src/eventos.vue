<template>
    <div class="button-container">
      <h2 class="title">Evento Click</h2>
      <button 
        v-for="button in buttons" 
        :key="button.color"
        @click="mostrarAlerta(button.color)"
        class="action-button"
        :style="{ backgroundColor: button.bgColor }"
      >
        Botón {{ button.label }}
      </button>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        buttons: [
          { color: 'naranja', bgColor: 'orange', label: 'Naranja' },
          { color: 'azul', bgColor: 'blue', label: 'Azul' }
        ]
      }
    },
    methods: {
      mostrarAlerta(color) {
        alert(`El botón ${color} ha sido presionado`);
      }
    }
  }
  </script>
  
  <style scoped>
  .button-container {
    text-align: center;
    padding: 20px;
  }
  
  .title {
    margin-bottom: 20px;
    color: #ffffff;
  }
  
  .action-button {
    color: white;
    padding: 10px 20px;
    margin: 5px;
    border: none;
    border-radius: 4px;
    cursor: pointer;
    font-size: 16px;
    transition: background-color 0.3s ease;
  }
  
  .action-button:hover {
    opacity: 0.9;
  }
  </style>