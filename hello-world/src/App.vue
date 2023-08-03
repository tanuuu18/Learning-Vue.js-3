<template>
  <Greet name="Tanu" profile="Front-end Developer" />
  <Greet name="Shree" profile="Back-end Developer" />
  <Greet name="Tanushree" profile="Full Stack Developer" />
</template>

<script>
import Greet from "./components/Greet.vue";

export default {
  name: 'App',
  components: {
    Greet: Greet,
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
