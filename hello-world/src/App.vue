<template>
   <h2>{{ name }}</h2>
  <div>
    <!-- On clicking the button name will change to batman -->
     <!-- Multiple event object handler -->
    <button v-on:click="changeName($event), increment(1, $event)">Change name</button>
  </div>
   <h2>{{ count }}</h2>
  <div>
    <button @click="increment(1, $event)">Increment 1</button>
    <button @click="increment(5)">Increment 5</button>
    <button @click="decrement(1)">Decrement 1</button>
    <button @click="decrement(5)">Decrement 5</button>
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
    // Event object automatically passes in if you don't specify in argument
      changeName(event) {
      this.name = "Batman";
      console.log("Events", event);
    },
    increment(num,event) {
      this.count += num;
      console.log(event);
    },
    decrement(num) {
      this.count -= num;
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
