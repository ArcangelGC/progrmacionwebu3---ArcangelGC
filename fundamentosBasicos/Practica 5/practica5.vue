<template>
    <div class="card-container">
      <div class="card">
        <!-- Imagen de la card -->
        <img 
          src="https://via.placeholder.com/300x200" 
          alt="Imagen de ejemplo"
          class="card-image"
        >
        
        <!-- Contenido de la card -->
        <div class="card-content">
          <h3 class="card-title">{{ title }}</h3>
          <p class="card-description">{{ description }}</p>
          
          <!-- Botón de acción -->
          <button 
            class="card-button"
            @click="handleClick"
          >
            Ver más
          </button>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        title: "Mi Primer Card",
        description: "Esta es una tarjeta de ejemplo creada con Vue.js. Puedes personalizar el contenido y los estilos según tus necesidades."
      }
    },
    methods: {
      handleClick() {
        console.log('Botón clickeado!');
        // Aquí puedes agregar tu lógica para manejar el click
      }
    }
  }
  </script>
  
  <style scoped>
  .card-container {
    display: flex;
    justify-content: center;
    padding: 20px;
  }
  
  .card {
    width: 300px;
    border-radius: 10px;
    box-shadow: 0 4px 8px rgba(0,0,0,0.1);
    overflow: hidden;
    transition: transform 0.3s ease;
    background-color: white;
  }
  
  .card:hover {
    transform: translateY(-5px);
  }
  
  .card-image {
    width: 100%;
    height: 200px;
    object-fit: cover;
  }
  
  .card-content {
    padding: 15px 20px;
  }
  
  .card-title {
    margin: 0 0 10px 0;
    color: #333;
  }
  
  .card-description {
    font-size: 0.9em;
    color: #666;
    margin: 0 0 15px 0;
    line-height: 1.5;
  }
  
  .card-button {
    background-color: #42b983;
    color: white;
    border: none;
    padding: 10px 20px;
    border-radius: 5px;
    cursor: pointer;
    transition: background-color 0.3s ease;
  }
  
  .card-button:hover {
    background-color: #3aa876;
  }
  </style>