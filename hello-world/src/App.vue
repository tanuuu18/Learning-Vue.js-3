<template>
   <h2>{{ name }}</h2>
  <div>
    <!-- On clicking the button name will change to batman -->
    <button v-on:click="name = 'Batman'">Change name</button>
  </div>
</template>

<script>


export default {
  name: 'App',
  data(){
    return {
        name: "Tanu",
    };
  },
   methods: {
  },
};
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
