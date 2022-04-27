<template>
  <div class="col-3 text-center my-5">
   
      <h3 class="my-3">{{serie.name}}</h3>
      <h4 class="my-3">{{serie.original_name}}</h4>
      <span class="fw-bolder my-3">{{serie.original_language}}</span>
      <h5>{{serie.vote_average}}</h5>
      
  </div>
</template>

<script>
export default {
  
  name: 'CardSerie',
  props: {
    serie: Object
  }
}
</script>

<style scoped >
 
</style>