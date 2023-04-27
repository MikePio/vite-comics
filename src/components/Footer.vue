<script>
export default {
  name: 'Footer',
  data(){
    return{
      
    }
  }
  
}
</script>

<template>
  <footer>
    <div class="container-top">
      
    </div>
    <div class="container-bottom col align-items-center justify-content-center">
      <div class="container row justify-content-between">
        <button>SIGN-UP NOW!</button>
        <div class="container-bottom-right row align-items-center">
          <h3>FOLLOW US</h3>
          <ul class="d-flex ">
            <li><img src="../assets/img/footer-facebook.png" alt="img-footer-down"></li>
            <li><img src="../assets/img/footer-twitter.png" alt="img-footer-down"></li>
            <li><img src="../assets/img/footer-youtube.png" alt="img-footer-down"></li>
            <li><img src="../assets/img/footer-pinterest.png" alt="img-footer-down"></li>
            <li><img src="../assets/img/footer-periscope.png" alt="img-footer-down"></li>
          </ul>
        </div>

      </div>

    </div>
  </footer>
</template>

<style lang="scss" scoped>
@use '../scss/main.scss' as *;

footer{
  .container-top{
    height: 370px;
    background-image: url('../assets/img/footer-bg.jpg');
  }

  .container-bottom{
    height: 100px;
    background-color: $quinary-color;

    .container-bottom-right{

      h3{
        color: $primary-color;
      }
    }

    button{
      background-color: transparent;
      background-repeat: no-repeat;
      cursor: pointer;
      overflow: hidden;
      outline: none;
      color: $tertiary-color;
      border: 3px $primary-color solid;
      font-size: 16px;
      padding: 10px;
      cursor: pointer;
    }
    ul{
      li{
        margin: 0 10px;
        &:hover{
          cursor: pointer;
        }
      }
    }

  }
}


</style>