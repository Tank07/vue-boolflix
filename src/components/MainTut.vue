<template>

<div class="bg_blacky">
  <div class="row" >
    
    <FilmList :propsArrayFilms2="propsArrayFilms" :propsArraySerie2="propsArraySerie"  />

  </div>

</div>


</template>

<script>

import FilmList from './FilmList.vue'

export default {
  
  name: 'MainTut',
  components: {
    FilmList
  },
  props:{
      propsArrayFilms: Array,
      propsArraySerie: Array
      
    }
}

</script>

<style scoped >

.bg_blacky{
  background-color: #141414;
}

</style>