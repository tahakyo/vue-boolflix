<template>
  <div id="app">
    <!-- header -->
    <header>
      <AppHeader @userInput="searchMovies($event)" />
    </header>
    <!-- header -->
    <!-- main -->
    <main>
      <AppMain :movies="moviesList" />
    </main>
    <!-- main -->
  </div>
</template>

<script>
import AppHeader from "./components/AppHeader.vue";
import AppMain from "./components/AppMain.vue";
import axios from "axios";
export default {
  name: "App",
  components: {
    AppHeader,
    AppMain,
  },
   data() {
    return {
      moviesList: [],
    };
  },
  methods: {
    searchMovies(input) {
      axios
      .get("https://api.themoviedb.org/3/search/movie", {
        params: {
          api_key: "d79e37bb8a27f3c75678e1bc5adf64dc",
          query: input,
        },
      })
      .then((resp) => {
        console.log(resp);
        this.moviesList = resp.data.results;
      })
    }
  },
};
</script>

<style lang="scss">
@import "./components/style/common.scss";
</style>
