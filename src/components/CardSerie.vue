<template>
  <div class="col-4 text-center my-3">

      <div class="flip-card">
        <div class="flip-card-inner">
          <div class="flip-card-front">
            <img :src="`https://image.tmdb.org/t/p/w342//${serie.poster_path}`" alt="" style="">
          </div>
          <div class="flip-card-back">
            <h3 class="my-3"> <span class="red fw-bold">Title</span> - {{serie.name}}</h3>
            <h5 class="my-3"><span class="red fw-bold">Original Title</span> - {{serie.original_name}}</h5>
            <h5>{{serie.vote_average}}</h5>
            <span class="flag"  :class="(serie.original_language == 'it') ? 'flag-it' : (serie.original_language == 'en') ? 'flag-en' : 'flag-boh'"></span>
            <h6><span class="red fw-bold">Plot</span> - {{serie.overview}}</h6>
            <p><i class="fa-star" v-for="i in 5" :key="i" :class="(i <= stars()) ? 'fa-solid' : 'fa-regular'" ></i></p>
          </div>
        </div>
      </div>

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