<template>
  <div id="app">
    <div>
      <input v-model="inputText" />
    </div>
    <div>
      <!-- Set the radius and text field of the svg circle  -->
      <svgcircle :radius="80" :text="inputText" />
    </div>
    <div>
      <svgcircle :radius="140" :text="inputText" />
    </div>
  </div>
</template>

<script>
import svgcircle from './components/svgcircle.vue'

export default {
  name: 'app',
  components: {
    svgcircle
  },
  data() {
		return {
      inputText: "Sample Text"
    };
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
