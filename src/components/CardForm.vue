<template>
  <div class="col-3 text-center my-5">
   
      <img :src="`https://image.tmdb.org/t/p/w342//${film.poster_path}`" alt="">
      <h3 class="my-3">{{film.title}}</h3>
      <h4 class="my-3">{{film.original_title}}</h4>
      <span class="fw-bolder my-3">{{film.original_language}}</span>
      <h5>{{film.vote_average}}</h5>
      <!-- <span class="flag"  :class="(film.original_language == `it`) ? `flag-it` : (film.original_language = `en`) ? `flag-en` : `flag-boh`"></span> -->
  </div>
</template>

<script>
export default {
  
  name: 'CardForm',
  props: {
    film: Object
  }
}
</script>

<style scoped >

 
</style>