<template>
  <div id="app">
    <NinjaCat :msg="gato"/>
  </div>
</template>

<script>
import NinjaCat from './components/NinjaCat.vue'

export default {
  name: 'App',
  components: {
    NinjaCat
  },
  data() {
    return {
      gato: "cat",
      ninja: "ninja"
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  color: #2c3e50;
  display: grid;
  place-items: center;
  background: linear-gradient(to bottom, rgba(194, 207, 215, 0.787) 0%, rgba(156, 163, 181, 0.698) 48%, rgba(87, 92, 101, 0.733) 100%);
  height: 100vh;
}
img {
  height: 450px;
}
button {
  margin: 40px;
}
</style>
