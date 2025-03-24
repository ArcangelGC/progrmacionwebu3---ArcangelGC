<template>
    <div class="card">
      <div class="card-header">
        {{ title }}
      </div>
      <div class="card-body">
        {{ body }}
      </div>
    </div>
  </template>
  
  <script>
  export default {
    name: 'HelloWorld',
    props: {
      title: {
        type: String,
        required: true
      },
      body: {
        type: String,
        required: true
      }
    }
  }
  </script>
  
  <style scoped>
  .card {
    border: 1px solid #ccc;
    border-radius: 8px;
    width: 300px;
    box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
    overflow: hidden;
  }
  
  .card-header {
    background-color: #f8f9fa;
    padding: 15px;
    font-size: 1.25rem;
    font-weight: bold;
    border-bottom: 1px solid #ccc;
  }
  
  .card-body {
    padding: 15px;
    font-size: 1rem;
    line-height: 1.5;
  }
  </style>