<script>
  export default {
    name: 'Card',
    props:{
      imgSrc: String,
      nameSerie: String,
    },
    data(){
      return{
        // dataJson
      }
    }
    
  }
</script>

<template>
  <div class="card col">
    <img :src="imgSrc" :alt="nameSerie">
    <div>{{ nameSerie }}</div>
  </div>
  
</template>
<style lang="scss" scoped>
  @use '../../scss/main.scss' as *;

  .card{
    height: 230px;
    width: 180px;
    color: $tertiary-color;
    margin: 30px 10px;
    &:hover{
      color: $primary-color;
      cursor: pointer;
    }
    img{
      height: 180px;
      width: 180px;
      margin-bottom: 15px;
    }
  }

</style>