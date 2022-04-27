<template>
  <div class="col-3 text-center my-3">
   
      <img :src="`https://image.tmdb.org/t/p/w185//${film.poster_path}`" alt="">
      <h3 class="my-3">{{film.title}}</h3>
      <h4 class="my-3">{{film.original_title}}</h4>
      <h5>{{film.vote_average}}</h5>
      <span class="flag"  :class="(film.original_language == 'it') ? 'flag-it' : (film.original_language == 'en') ? 'flag-en' : 'flag-boh'"></span>
      <p><i class="fa-star" v-for="i in 5" :key="i" :class="(i <= stars()) ? 'fa-solid' : 'fa-regular'" ></i></p>
  </div>
</template>

<script>
export default {
  
  name: 'CardForm',
  props: {
    film: Object
  },

  methods: {
    stars(){
      let roundedRating = Math.ceil(this.film.vote_average)/2
      return roundedRating
    }
  }
}
</script>


<style >

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