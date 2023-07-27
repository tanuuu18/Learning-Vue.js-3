<template>
 <h2>Fullname - {{ firstName }} {{ lastName }}</h2>
  <h2>Computed fullname: {{ fullName }}</h2>
</template>

<script>


export default {
  name: 'App',
  data(){
    return {
       firstName: "Tanu",
      lastName: "Shree",
    };
  },
   methods: { },
  computed: {
    fullName() {
      return `${this.firstName} ${this.lastName}`;
    },
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /* text-align: center; */
  color: #2c3e50;
  margin-top: 60px;
}

</style>
