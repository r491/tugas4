<template>
  <div id="app">
    <header>
      <h1>Nested & Slot Components Example</h1>
    </header>
    <main>
      <div class="container">
        <ParentComponent />
      </div>
    </main>
  </div>
</template>

<script>
import ParentComponent from './ParentComponent.vue'

export default {
  name: 'App',
  components: {
    ParentComponent
  }
}
</script>

<style>
#app {
  font-family: 'Arial', sans-serif;
  text-align: center;
}

header {
  background-color: #000000;
  color: white;
  padding: 20px;
}

.container {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
}

main {
  flex: 1;
}
</style>
