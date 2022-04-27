<template>

<div>
  <div class="row" >
    
    <CardForm
      v-for="( element, index ) in propsArrayFilms2"
      :key="index"
      :film="element"
    />

  </div>

  <div class="row">

    <CardSerie
      v-for="( element, index ) in propsArraySerie2"
      :key="index"
      :serie="element"
    />

  </div>

</div>


</template>

<script>

import CardForm from './CardForm.vue'
import CardSerie from './CardSerie.vue'

export default {
  
  name: 'FilmList',
  components: {
    CardForm,
    CardSerie
  },
  props:{
      propsArrayFilms2: Array,
      propsArraySerie2: Array
      
    }
}


</script>

<style scoped >

</style>