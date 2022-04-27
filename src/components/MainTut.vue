<template>

<div>
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

</style>