<template> <!--The template for our page-->
  <div id="app">
    <Dealers />
  </div>
</template>

<script> //Logic of component
import Dealers from './components/Dealers.vue'

export default {
  name: 'app',
  components: {
    Dealers
  }
}
</script>

<style> /*The Styles for our page*/
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
