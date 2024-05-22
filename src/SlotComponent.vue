<!-- SlotComponent.vue -->
<template>
  <div class="slot-container">
    <h2 class="slot-title">Slot Component</h2>
    <div class="slot-content">
      <slot></slot>
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style scoped>
.slot-container {
  background-color: #f9f9f9;
  border-radius: 8px;
  padding: 20px;
  margin-top: 20px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}

.slot-title {
  color: #333;
  margin-bottom: 10px;
}

.slot-content {
  color: #666;
}
</style>
