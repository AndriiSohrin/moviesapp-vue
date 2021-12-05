<template>
  <div id="app">
    <MoviesList :list="moviesList" />
  </div>
</template>

<script>
import { mapActions, mapGetters } from "vuex";
import MoviesList from "./components/MoviesList";

export default {
  name: "App",
  components: {
    MoviesList
  },
  computed: {
    ...mapGetters("moviesStore", ["moviesList"])
  },
  mounted() {
    // this.fetchMovies();

  },
  methods: {
    ...mapActions("moviesStore", ["fetchMovies"])
  }
};
</script>

<style>
#app {
  font-family: Arial, Helvetica, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
</style>
