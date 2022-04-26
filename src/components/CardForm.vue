<template>
  <div class="col-3 text-center my-5">
   
      <h3 class="my-3">{{film.title}}</h3>
      <h4 class="my-3">{{film.original_name}}</h4>
      <span class="fw-bolder my-3">{{film.original_language}}</span>
      <h5>{{film.vote_average}}</h5>
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
 
</style>