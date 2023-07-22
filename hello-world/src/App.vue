<template>
   <h2>{{ name }}</h2>
  <div>
    <!-- On hovering the button name will change to batman -->
    <button v-on:mouseover="name = 'Batman'">Change name</button>
  </div>
   <h2>{{ count }}</h2>
  <div>
     <!--Here we used Inline event handlers -->
    <button v-on:click="increment">Increment</button>
    <button v-on:click="decrement">Decrement</button>
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
      increment() {
      this.count += 1;
    },
    decrement() {
      this.count -= 1;
    },
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
