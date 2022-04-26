<template>

<div>
  <div class="row" >
    
    <FilmList :propsArrayFilms2="propsArrayFilms"    />

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
      propsArrayFilms: Array
      
    }
}

</script>

<style scoped >

</style>