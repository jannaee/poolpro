<template> 
  <div class="hello">
    {{name}}<!--Interpolation is defining a string-->
    {{btnState ? 'The button is disabled' : 'The button is active'}}<!--Interpolation with expression-->

    <button v-on:click="changeName" v-bind:disabled="btnState" >Change Name</button>
    <div class="holder">
      <ul>
        <li v-for="(data, index) in skills" :key='index'>{{ index }}. {{ data.skill }}</li>
      </ul>
      <h2 v-if="skills.length >= 1">You have more than 1 skills</h2>
      <h2 v-else>Time to turn up the studying</h2>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Dealers',
  data() {
    return {
      name: 'Coursetro',
      btnState: true, //This is an example of interpolation within attributes,
      skills : [
        {"skill": "Vue.js"}
      ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
