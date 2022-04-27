<template>
  <div class="col-3 text-center my-5">

      <img :src="`https://image.tmdb.org/t/p/w342//${serie.poster_path}`" alt="">
      <h3 class="my-3">{{serie.name}}</h3>
      <h4 class="my-3">{{serie.original_name}}</h4>
      <span class="fw-bolder my-3">{{serie.original_language}}</span>
      <h5>{{serie.vote_average}}</h5>
      <span class="flag"  :class="(serie.original_language == 'it') ? 'flag-it' : (serie.original_language == 'en') ? 'flag-en' : 'flag-boh'"></span>
  </div>
</template>

<script>
export default {
  
  name: 'CardSerie',
  props: {
    serie: Object
  }
}
</script>

<style scoped >
 
</style>