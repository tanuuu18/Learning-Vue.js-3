<template>
  
  <!-- Conditional rendering -->
  <h2 v-if="num === 0">The number is zero</h2>
  <h2 v-else-if="num < 0">The number is negative</h2>
  <h2 v-else-if="num > 0">The number is positive</h2>
  <h2 v-else>Not a number</h2>

  <!-- Conditional rendering multiple elements -->
  <!-- change this div to template tag then we will not see additional div tag in DOM. -->
  <template v-if="display">
    <h2>Tanushree</h2>
    <h2>Software Developer</h2>
    <h2>Vue</h2>
  </template>
  
</template>

<script>


export default {
  name: 'App',
  data(){
    return {
     num: "Hi",
      display: true,
     },
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
