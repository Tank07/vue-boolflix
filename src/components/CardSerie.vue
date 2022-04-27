<template>
  <div class="col-3 text-center my-3">

      <img class=""
       :src="`https://image.tmdb.org/t/p/w185//${serie.poster_path}`" alt="">
      <h3 class="my-3">{{serie.name}}</h3>
      <h4 class="my-3">{{serie.original_name}}</h4>
      <span class="fw-bolder my-3">{{serie.original_language}}</span>
      <h5>{{serie.vote_average}}</h5>
      <span class="flag"  :class="(serie.original_language == 'it') ? 'flag-it' : (serie.original_language == 'en') ? 'flag-en' : 'flag-boh'"></span>
      <p><i class="fa-star" v-for="i in 5" :key="i" :class="(i <= stars()) ? 'fa-solid' : 'fa-regular'" ></i></p>
  </div>
</template>

<script>
export default {
  
  name: 'CardSerie',
  props: {
    serie: Object
  },

  methods: {
    stars(){
      let roundedRating = Math.ceil(this.serie.vote_average)/2
      return roundedRating
    }
  }
}
</script>

<style scoped >
 
</style>