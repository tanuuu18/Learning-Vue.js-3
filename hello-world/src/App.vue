<template>
 
<!-- composed new data properties from existing properties -->
 <h2>Fullname - {{ firstName }} {{ lastName }}</h2>
  <h2>Computed fullname: {{ fullName }}</h2>
<button @click="items.push({ id: 4, title: 'Keyboard', price: 50 })">
    Add Item
  </button>
   <!-- can be used at multiple places at multiple times -->
 <!-- Computed properties automatically recalculated when the dependency have changed -->
  <h2>Computed Total : {{ total }}</h2>
</template>

<script>


export default {
  name: 'App',
  data(){
    return {
       firstName: "Tanu",
      lastName: "Shree",
     items: [
        {
          id: 1,
          title: "TV",
          price: 100,
        },
        {
          id: 2,
          title: "Phone",
          price: 200,
        },
        {
          id: 3,
          title: "Laptop",
          price: 300,
        },
      ],
    };
  },
   methods: { },
  computed: {
    fullName() {
      return `${this.firstName} ${this.lastName}`;
    },
    total() {
      return this.items.reduce(
        (total, curr) => (total = total + curr.price),
        0
      );
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
