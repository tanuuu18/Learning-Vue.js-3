<template>
   <h2>Volume Tracker (0-20)</h2>
  <h2>Current Volume - {{ volume }}</h2>

  <div>
    <button @click="volume += 2">Increase</button>
    <button @click="volume -= 2">Decrease</button>
  </div>
   <input type="text" v-model="movie" />
    <input type="text" v-model="movieInfo.title" />
  <input type="text" v-model="movieInfo.actor" />
  <div><button @click="movieList.push('Wonder women')">Add movie</button></div>
</template>

<script>


export default {
  name: 'App',
  data(){
    return {
      volume: 0,
       //After setting this value the api will not call
      movie: "Tanu",
       movieInfo: {
        title: "",
        actor: "",
      },
      movieList: ["Batman", "Superman"],
    },
   methods: { },
  computed: { },
   //Watchers executed only when the data has changed
 watch: {
    volume(newValue, oldValue) {
     //Will show alert on 16 while increaseing volume not on decresing
      if (newValue > oldValue && newValue === 16) {
        alert(
          "Listening to a high volume for a long time may damage your hearing"
        );
      }
    },
    movie(newValue) {
      console.log(`Calling an API with movie name = ${newValue}`);
    },
    movieInfo: {
      handler(newValue) {
        console.log(
          `Calling an API with movie title = ${newValue.title} and actor = ${newValue.actor}`
        );
      },
      deep: true,
    },
    movieList: {
      handler(newValue) {
        console.log(`Updated list ${newValue}`);
      },
      deep: true,
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
