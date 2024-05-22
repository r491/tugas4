<!-- ChildComponent.vue -->
<template>
    <div class="child-container">
      <h2 class="child-title">Child Component</h2>
      <button @click="emitData" class="child-button">Send Data to Parent</button>
    </div>
  </template>
  
  <script>
  export default {
    methods: {
      emitData() {
        const data = "Ini data dari child component"
        this.$emit('dataUpdated', data)
      }
    }
  }
  </script>
  
  <style scoped>
  .child-container {
    background-color: #e0e0e0;
    border-radius: 8px;
    padding: 15px;
    margin-bottom: 20px;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  }
  
  .child-title {
    color: #333;
  }
  
  .child-button {
    background-color: #4CAF50;
    color: white;
    border: none;
    border-radius: 4px;
    padding: 10px 20px;
    cursor: pointer;
    transition: background-color 0.3s;
  }
  
  .child-button:hover {
    background-color: #45a049;
  }
  </style>
  