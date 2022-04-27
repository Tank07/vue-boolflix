<template>
  <div class=" col-4 text-center my-3">

    <div class="flip-card">
      <div class="flip-card-inner">
        <div class="flip-card-front">
          <img :src="`https://image.tmdb.org/t/p/w342//${film.poster_path}`" alt="" style="">
        </div>
        <div class="flip-card-back">
          <h3 class="my-3"> <span class="red fw-bold">Title</span> - {{film.title}}</h3>
          <h5 class="my-3"><span class="red fw-bold">Original Title</span> - {{film.original_title}}</h5>
          <h5>{{film.vote_average}}</h5>
          <span class="flag"  :class="(film.original_language == 'it') ? 'flag-it' : (film.original_language == 'en') ? 'flag-en' : 'flag-boh'"></span>
          <h6><span class="red fw-bold">Plot</span> - {{film.overview}}</h6>
          <p><i class="fa-star" v-for="i in 5" :key="i" :class="(i <= stars()) ? 'fa-solid' : 'fa-regular'" ></i></p>
        </div>
      </div>
    </div>
      
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

.red{
  color: #E50914;
}

.flag{
  display: inline-block;
  height: 35px;
  width: 35px;
  background-size: contain;
}

.flag-it{
  background-image: url("../assets/icons8-italia-48.png");
}

.flag-en{
  background-image: url("../assets/icons8-gran-bretagna-48.png");
}

.flag-boh{
  background-image: url("../assets/icons8-punto-interrogativo-48.png");
  /* background-color: #E1D9D1; */
}

/* Flip card from W3School */

.flip-card {
  background-color: transparent;
  width: 344px;
  height: 515px;
  border: 1px solid #f1f1f1;
  perspective: 1000px; /* Remove this if you don't want the 3D effect */
}

/* This container is needed to position the front and back side */
.flip-card-inner {
  position: relative;
  width: 100%;
  height: 100%;
  text-align: center;
  transition: transform 0.8s;
  transform-style: preserve-3d;
}

/* Do an horizontal flip when you move the mouse over the flip box container */
.flip-card:hover .flip-card-inner {
  transform: rotateY(180deg);
}

/* Position the front and back side */
.flip-card-front, .flip-card-back {
  position: absolute;
  width: 100%;
  height: 100%;
  -webkit-backface-visibility: hidden; /* Safari */
  backface-visibility: hidden;
}

/* Style the front side (fallback if image is missing) */
.flip-card-front {
  background-color: #141414;
  color: black;
}

/* Style the back side */
.flip-card-back {
  background-color: #141414;
  color: white;
  transform: rotateY(180deg);
  overflow-y: auto;
}

 
</style>