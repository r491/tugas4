<!-- ParentComponent.vue -->
<template>
    <div class="parent-container">
      <h1 class="parent-title">Parent Component</h1>
      <div class="parent-content">
        <ChildComponent @dataUpdated="handleDataUpdate" />
        <hr />
        <h2>Data dari Child Component:</h2>
        <p>{{ childData }}</p>
      </div>
      <hr />
      <div class="slot-container">
        <h2>Slot Content</h2>
        <SlotComponent>
          <p>Ini Contoh Slot</p>
        </SlotComponent>
      </div>
    </div>
  </template>
  
  <script>
  import ChildComponent from './ChildComponent.vue'
  import SlotComponent from './SlotComponent.vue'
  
  export default {
    components: {
      ChildComponent,
      SlotComponent
    },
    data() {
      return {
        childData: ''
      }
    },
    methods: {
      handleDataUpdate(data) {
        this.childData = data
      }
    }
  }
  </script>
  
  <style scoped>
  .parent-container {
    background-color: #f0f0f0;
    border-radius: 10px;
    padding: 20px;
    margin: 20px;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  }
  
  .parent-title {
    color: #333;
  }
  
  .parent-content {
    margin-top: 20px;
  }
  
  .slot-container {
    margin-top: 20px;
  }
  </style>
  