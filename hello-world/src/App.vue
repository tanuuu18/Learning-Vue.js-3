<template>
  <!-- Text interpolation -->
  <div>{{greet}} {{name}}</div>
  <!-- Using Directives -->
  <div v-html="learning"></div>
</template>

<script>


export default {
  name: 'App',
  data(){
    return {
      greet:"Hello",
      name:"Tanushree",
      learning:"<b>Vue Js</b>"
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
