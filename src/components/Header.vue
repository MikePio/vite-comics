<script>
export default {
  name: 'Header',
  data(){
    return{

    }
  }
}
</script>

<template>
  <header class="d-flex col align-items-center justify-content-center">
    <div class="container-header container d-flex justify-content-between align-items-center">
      <div class="nav-row row justify-content-between align-items-center ">
        
        <div class="row-logo row align-items-center">
            <img class="logo" src="../assets/img/dc-logo.png" alt="">
          </div>

          <div class="row justify-content-end">
          <ul class="nav-list d-flex ">
            <li>CHARACTERS</li>
            <li>COMICS</li>
            <li>MOVIES</li>
            <li>TV</li>
            <li>GAMES</li>
            <li>COLLECTIBLES</li>
            <li>VIDEOS</li>
            <li>FANS</li>
            <li>NEWS</li>
            <li>SHOP</li>
          </ul>
        </div>

      </div>
    </div>
  </header>
  
</template>

<style lang="scss" scoped>
// @use '../scss/partials/_var.scss';
@use '../scss/main.scss' as *;

header{
  width: 100%;
  height: 110px;
  background-color: $tertiary-color;
  padding: 15px;
  img{
    height: 80px;
    min-height: 80px;
  }
  .logo{
    cursor: pointer;
  }
    
}

ul{
  
  li{
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    height: 110px;
    margin: 0 10px;
    font-size: small;
    color: $quinary-color;
    font-weight: 600;
    border-bottom: 6px solid transparent;
    &:hover{
      cursor: pointer;
      color: $primary-color;
      border-bottom: 6px solid $primary-color;
    }
  }

}

.container-header{
  width: 85%;
}

.nav-row{
  width: 100%;
}

.row-logo{
  width: 25%;
}

.nav-list{

}























</style>