<template>
  <div class="about">
    <h1>{{movie.name}}</h1>
    <div style="display: flex;">

        <img :src="'/images/'+movie.image">

        <div style="width: 50%; padding: 3%;"> 
        <p> Release Date: {{ movie.releaseDate }} </p>
        
        <p> Opening Gross: ${{ movie.openingGross }} </p>
        <p> Lifetime Gross: ${{movie.lifetimeGross}} </p>

      </div>
    </div>
    

    
    


  </div>
  
</template>

<script>

export default {
  name: 'Single-Movie-Comp',
  props: {
      movie: Object
  },
  
  // data() {
  //   return {
  //     country: '',
  //   }
  // },
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