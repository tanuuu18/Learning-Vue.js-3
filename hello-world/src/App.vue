<template>
  
  <h2 v-bind:id="headingId">Heading</h2>
  <button v-bind:disabled="isDisabled">Bind</button>
  <h2 class="underline">Underlined text</h2>
  <h2 v-bind:class="status">Status</h2>
</template>

<script>


export default {
  name: 'App',
  data(){
    return {
      headingId:"heading",
      isDisabled:true,
      status:"danger"
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
  .underline{
  text-decoration: underline;
}
</style>
