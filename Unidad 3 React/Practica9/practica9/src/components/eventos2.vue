<template>
    <div class="form-container">
      <h2 class="form-title">Evento Change</h2>
      
      <div class="input-group">
        <label for="nombreInput" class="input-label">Nombre:</label>
        <input
          id="nombreInput"
          v-model.trim="nombre"
          @change="guardarNombre"
          @keyup.enter="guardarNombre"
          placeholder="Ingresa tu nombre completo"
          class="form-input"
          :class="{ 'input-error': mostrarError }"
        >
        <span v-if="mostrarError" class="error-message">Por favor ingresa un nombre válido (mínimo 3 caracteres)</span>
      </div>
  
      <transition name="slide-fade">
        <div v-if="nombreGuardado" class="result-container">
          <h3 class="result-title">Información Guardada</h3>
          <div class="result-content">
            <p class="result-text">Nombre completo registrado:</p>
            <div class="name-display">{{ nombreGuardado }}</div>
          </div>
          <button @click="limpiarFormulario" class="clear-button">
            <i class="fas fa-trash-alt"></i> Limpiar Registro
          </button>
        </div>
      </transition>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        nombre: '',
        nombreGuardado: '',
        mostrarError: false
      };
    },
    methods: {
      guardarNombre() {
        if (this.nombre.length < 3) {
          this.mostrarError = true;
          return;
        }
        
        this.mostrarError = false;
        this.nombreGuardado = this.nombre;
      },
      limpiarFormulario() {
        this.nombre = '';
        this.nombreGuardado = '';
        this.mostrarError = false;
      }
    }
  }
  </script>
  
  <style scoped>
  .form-container {
    max-width: 1000px;
    margin: 0 auto;
    padding: 25px;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    background-color: #f8f9fa;
    border-radius: 0px;
    box-shadow: 0 2px 100px rgba(0, 0, 0, 0.1);
  }
  
  .form-title {
    color: #2c3e50;
    text-align: center;
    margin-bottom: 25px;
    font-size: 24px;
  }
  
  .input-group {
    margin-bottom: 20px;
  }
  
  .input-label {
    display: block;
    margin-bottom: 8px;
    font-weight: 600;
    color: #495057;
  }
  
  .form-input {
    width: 100%;
    padding: 12px 4px;
    border: 1px solid #ced4da;
    border-radius: 6px;
    font-size: 16px;
    transition: all 0.3s;
  }
  
  .form-input:focus {
    border-color: #42b983;
    outline: none;
    box-shadow: 0 0 0 3px rgba(66, 185, 131, 0.2);
  }
  
  .input-error {
    border-color: #ff0000;
  }
  
  .error-message {
    display: block;
    margin-top: 8px;
    color: #ff0000;
    font-size: 14px;
  }
  
  .result-container {
    margin-top: 50px;
    padding: 40px;
    border: 1px solid #e9ecef;
    border-radius: 8px;
    background-color: white;
    box-shadow: 0 1px 3px rgba(0, 0, 0, 0.05);
  }
  
  .result-title {
    color: #2c3e50;
    margin-top: 0;
    margin-bottom: 15px;
    font-size: 18px;
    border-bottom: 1px solid #eee;
    padding-bottom: 10px;
  }
  
  .result-content {
    margin-bottom: 10px;
  }
  
  .result-text {
    color: #6c757d;
    margin-bottom: 10px;
  }
  
  .name-display {
    padding: 15px;
    background-color: #000000;
    border-radius: 6px;
    font-size: 18px;
    line-height: 1.5;
    min-height: 10px;
    word-break: break-word;
    white-space: pre-wrap;
  }
  
  .clear-button {
    display: inline-flex;
    align-items: center;
    justify-content: center;
    width: 100%;
    padding: 10px;
    background-color: #ae0b0b;
    color: rgb(0, 0, 0);
    border: none;
    border-radius: 6px;
    font-size: 16px;
    cursor: pointer;
    transition: all 0.3s;
  }
  
  .clear-button:hover {
    background-color: #fa5252;
  }
  
  .clear-button i {
    margin-right: 8px;
  }
  
  /* Animaciones */
  .slide-fade-enter-active {
    transition: all 0.3s ease-out;
  }
  
  .slide-fade-leave-active {
    transition: all 0.2s cubic-bezier(1, 0.5, 0.8, 1);
  }
  
  .slide-fade-enter-from,
  .slide-fade-leave-to {
    transform: translateY(10px);
    opacity: 0;
  }
  </style>