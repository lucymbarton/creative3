<template>
  <div class="about">
    <h1>Harry Potter</h1>
    <span v-if="!isMovieSelected"> 
      <MovieList :movies="movies" />
    </span>
    <span v-else > 
      <Single-Movie-View :movie="selectedMovie"/>
    </span>
    
  </div>
  
</template>

<script>
import  MovieList  from '../components/MovieList.vue'
import SingleMovieView from '../components/SingleMovieView.vue'

export default {
  name: 'Movie-Comp',
  components: {
    MovieList,
    SingleMovieView
  },
  data() {
    return {
      isMovieSelected: false,
      selectedMovie: {}
    }
  },
  computed: {
    movies() {
      return this.$root.$data.movies
    }
  },
  // methods: {
  //   select(country) {
  //     this.country = country;
  //   }
  // }
}
</script>
