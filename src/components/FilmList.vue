<template>

<div>
  <div class="row" >
    
    <CardForm
      v-for="( element, index ) in propsArrayFilms2"
      :key="index"
      :film="element"
    />

  </div>

</div>


</template>

<script>

import CardForm from './CardForm.vue'

export default {
  
  name: 'FilmList',
  components: {
    CardForm
  },
  props:{
      propsArrayFilms2: Array
      
    }
}


</script>

<style scoped >

</style>