<template>
  <div id="app">

    <HeaderSearch @funzioneRicerca="metodoSearch"/>

    <MainTut :propsArrayFilms="films" :propsArraySerie="series"/>
    

  </div>
</template>

<script>

import "bootstrap"
import axios from 'axios';

import MainTut from './components/MainTut.vue'
import HeaderSearch from './components/HeaderSearch.vue'
// import DischiList from './components/DischiList.vue'

export default {
  name: 'App',
  components: {
     HeaderSearch,
     MainTut
    // DischiList
  },
   data(){
      return{
        testoRicerca: "",
        films:[],
        series:[]
          
    }
  }, 
  methods: {
    metodoSearch( testoricercato ){
      axios.get(`https://api.themoviedb.org/3/search/movie?api_key=e99307154c6dfb0b4750f6603256716d&query=${testoricercato}`)
            .then( (res) => {
              console.log(res.data.results);
              this.films = res.data.results
          }
            )
            axios.get(`https://api.themoviedb.org/3/search/tv?api_key=e99307154c6dfb0b4750f6603256716d&query=${testoricercato}`)
             .then( (res) => {
               console.log(res.data.results);
               this.series = res.data.results
             }
            )
      }
    } 
  }
</script>

<style lang="scss">

  @import "bootstrap/dist/css/bootstrap.min.css";

  

</style>