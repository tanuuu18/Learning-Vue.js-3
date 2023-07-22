<template>
   <h2>{{ name }}</h2>
  <div>
    <!-- On hovering the button name will change to batman -->
    <button v-on:mouseover="name = 'Batman'">Change name</button>
  </div>
   <h2>{{ count }}</h2>
  <div>
    <button v-on:click="count += 1">Increment</button>
    <button v-on:click="count -= 1">Decrement</button>
  </div>
</template>

<script>


export default {
  name: 'App',
  data(){
    return {
        name: "Tanu",
        count: 0,
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
