<template>
  <Greet name="Tanu" profile="Front-end Developer" />
  <Greet name="Shree" profile="Back-end Developer" />
  <Greet name="Tanushree" profile="Full Stack Developer" />
    <Greet :name="name" :profile="profile" />
</template>

<script>
import Greet from "./components/Greet.vue";

export default {
  name: 'App',
  components: {
    Greet: Greet,
  },
   //Using data binding
  data() {
    return {
      name: "Tanu",
      profile: "MERN Developer",
    };
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
