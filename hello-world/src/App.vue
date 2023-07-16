<template>
  <!-- Text interpolation -->
  <div>{{greet}} {{name}}</div>
  <!-- Binding HTML -->
  <div v-html="learning"></div>
  <div v-html="hack"></div>
  <h2 v-bind:id="headingId">Heading</h2>
  <button v-bind:disabled="isDisabled">Bind</button>
</template>

<script>


export default {
  name: 'App',
  data(){
    return {
      greet:"Hello",
      name:"Tanushree",
      learning:"<b>Vue Js</b>",
      hack:`<a href="#" onclick="alert('You have been hacked!')">Win a Prize</a>`,
      headingId:"heading",
      isDisabled:true
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
