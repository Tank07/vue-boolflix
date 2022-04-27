<template>
  <div class="d-flex justify-content-between">

    <div class="px-2">
      <img src="../assets/netflix-logo.png" alt="">
    </div>
    
    <form action="" class="d-flex py-2">
      <input
        type="text"
        class="form-control "
        v-model="searchText">
      <button 
        type="submit"
        class="btn "
        @click.prevent="$emit( 'funzioneRicerca', searchText )"
      ><i class="fa-solid fa-magnifying-glass text-white"></i></button>
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
    background-color: #0a0a0a;
}

img{
  height: 50px;
  width: auto;
}

</style>