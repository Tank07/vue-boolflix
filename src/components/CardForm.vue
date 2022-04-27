<template>
  <div class="col-3 text-center my-5">
   
      <img :src="`https://image.tmdb.org/t/p/w342//${film.poster_path}`" alt="">
      <h3 class="my-3">{{film.title}}</h3>
      <h4 class="my-3">{{film.original_title}}</h4>
      <!-- <span class="fw-bolder my-3">{{film.original_language}}</span> -->
      <h5>{{film.vote_average}}</h5>
      <span class="flag"  :class="(film.original_language == 'it') ? 'flag-it' : (film.original_language == 'en') ? 'flag-en' : 'flag-boh'"></span>
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

.flag{
  display: inline-block;
  height: 25px;
  width: 25px;
  background-size: contain;
}

.flag-it{
  background-image: url("../assets/icons8-italia-48.png");
}

.flag-en{
  background-image: url("../assets/icons8-gran-bretagna-48.png");
}

.flag-boh{
  background-image: url("../assets/icons8-decisione-100.png");
  /* background-color: #E1D9D1; */
}

 
</style>