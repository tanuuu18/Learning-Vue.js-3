<template>
 
<!-- composed new data properties from existing properties -->
 <h2>Fullname - {{ firstName }} {{ lastName }}</h2>
  <h2>Computed fullname: {{ fullName }}</h2>
<button @click="items.push({ id: 4, title: 'Keyboard', price: 50 })">
    Add Item
  </button>
   <!-- can be used at multiple places at multiple times -->
 <!-- Computed properties automatically recalculated when the dependency have changed -->
 <!-- Both(Computed and method) will return same result.Buth difference is that
  Computed properties are cached, this increase App performance -->
  <h2>Computed Total : {{ total }}</h2>

  <h2>Method Total - {{ getTotal() }}</h2>
  <!-- as we type in input, only getTotal method is recalculated not computed -->
  <input type="text" v-model="country" />
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
      country: "",
    };
  },
   methods: {
    getTotal() {
      console.log("getTotal method");
      return this.items.reduce(
        (total, curr) => (total = total + curr.price),
        0
      );
    },
   },
  computed: {
    fullName() {
      return `${this.firstName} ${this.lastName}`;
    },
    total() {
      console.log("total computed property");
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
