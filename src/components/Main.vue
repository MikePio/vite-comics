<script>
export default {
  name: 'Main',
  data(){
    return{

    }
  }
}
</script>

<template>
  <body class="d-flex col align-items-center">
    <div class="container-content col justify-content-center align-items-center">
      <div class="container row align-items-center">
        <h1><span>--</span>> Content goes here <span>&lt--</span></h1>

      </div>
    </div>
    
    <div class="container-cta col justify-content-center align-items-center">
      <div class="container row align-items-center justify-content-around">
        <div class="col">
          <div class="item-cta row align-items-center">
            <div class="col">
              <img src="../assets/img/buy-comics-digital-comics.png" alt="img">
            </div>
            <div class="col justify-content align-items-center">
              <div>digital comics</div>
            </div>
          </div>
        </div>
        <div class="col">
          <div class="item-cta row align-items-center">
            <div class="col">
              <img src="src\assets\img\buy-comics-merchandise.png" alt="img">
            </div>
            <div class="col">
              <div>dc merchandise</div>
            </div>
          </div>
        </div>
        <div class="col">
          <div class="item-cta row align-items-center">
            <div class="col">
              <img src="src\assets\img\buy-comics-subscriptions.png" alt="img">
            </div>
            <div class="col justify-content align-items-center">
              <div>subscription</div>
            </div>
          </div>
        </div>
        <div class="col">
          <div class="item-cta row align-items-center">
            <div class="col">
              <img class="position-img" src="src\assets\img\buy-comics-shop-locator.png" alt="img">
            </div>
            <div class="col justify-content align-items-center">
              <div>comic shop locator</div>
            </div>
          </div>
        </div>
        <div class="col">
          <div class="item-cta row align-items-center">
            <div class="col">
              <img class="visa-img" src="../assets/img/buy-dc-power-visa.svg" alt="img-visa">
            </div>
            <div class="col justify-content align-items-center">
              <div>dc power visa</div>
            </div>
          </div>
        </div>
      </div>
    </div>
  
  </body>

</template>

<style lang="scss" scoped>
  @use '../scss/main.scss' as *;

  h1{
    color: $tertiary-color;
  }

  body{
    .container-content{
      width: 100%;
      height: 110px;
      background-color: $senary-color;
    }
    .container-cta{
      width: 100%;
      // max-width: 100%;
      height: 150px;
      background-color: $primary-color;
      .container{
        
      }
    }
  }

  .item-cta{
    color: $tertiary-color;
    text-transform: uppercase;
    img{
      width: 40px;
      margin-right: 8px;
    }
    
    .position-img{
      width: auto;
      height: 40px;
    }
      
  }








</style>