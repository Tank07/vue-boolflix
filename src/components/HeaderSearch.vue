<template>
  <div>
    
    <form action="" class="d-flex">
      <input
        type="text"
        class="form-control me-5"
        v-model="searchText">
      <button
        type="submit"
        class="btn btn-primary"
        @click.prevent="$emit( 'funzioneRicerca', searchText )"
      >Ricerca</button>
    </form>
  </div>

</template>

<script>
export default {
  
  name: 'HeaderSearch',
  data(){
    return{
      searchText: ''
    }
  }
}
</script>

<style scoped >

div{
    background-color: black;
}

</style>