<script>
// import
  // { linksFooterTop} from "../data/footer-top",
  // { linksFooterBottom} from "../data/footer-bottom"
  // { linksFooterBottom} from "../data/footer-bottom"
  // { linksFooterTop, linksFooterBottom} from "../data/footer-top" from "../data/footer-bottom"
  import { linksFooterTop} from "../data/footer-top";
  import { linksFooterBottom} from "../data/footer-bottom"
export default {
  name: 'Footer',
  data(){
    return{
      linksFooterTop,
      linksFooterBottom
    }
  }
  
}
</script>

<template>
  <footer>

    <div class="container-top col align-items-center justify-content-center">
      <div class="big-container container row ">
        <div class="half-container half-container-left">
          <div class="row">
            <div class="col">
              
              <ul>
                <h4>DC COMICS</h4>
                <li v-for="(listItem, index) in linksFooterTop[0].dcComics" :key="index"><a :href="`${listItem.url}`">{{ listItem.name }}</a></li>
                <!-- <li>Characters</li>
                <li>Comics</li>
                <li>Movies</li>
                <li>TV</li>
                <li>Games</li>
                <li>Videos</li>
                <li>News</li> -->
              </ul>
  
              <ul>
                <h4>SHOP</h4>
                <li v-for="(listItem, index) in linksFooterTop[1].shop" :key="index"><a :href="`${listItem.url}`">{{ listItem.name }}</a></li>
                <!-- <li>Shop DC</li>
                <li>Shop DC Collectibles</li> -->
              </ul>
            </div>
    
            <div class="col">
              <ul>
                <h4>DC</h4>
                <li v-for="(listItem, index) in linksFooterTop[2].dc" :key="index"><a :href="`${listItem.url}`">{{ listItem.name }}</a></li>
                <!-- <li>Terms Of Use</li>
                  <li>Privacy policy (New)</li>
                <li>Ad Choices</li>
                <li>Advertising</li>
                <li>Jobs</li>
                <li>Subscriptions</li>
                <li>Talent Workshops</li>
                <li>CPSC Certificates</li>
                <li>Ratings</li>
                <li>Shop Help</li>
                <li>Contact Us</li> -->
              </ul>
            </div>
    
            <div class="col">
              <ul>
                <h4>SITES</h4>
                <li v-for="(listItem, index) in linksFooterTop[3].sites" :key="index"><a :href="`${listItem.url}`">{{ listItem.name }}</a></li>
                <!-- <li>DC</li>
                <li>MAD Magazine</li>
                <li>DC Kids</li>
                <li>DC Universe</li>
                <li>DC Power Visa</li> -->
              </ul>
            </div>
              
          </div>
            
      </div>
        <div class="half-container half-container-right">
          <!-- <img class="dc-background" src="../assets/img/dc-logo-bg.png" alt="dc-background"> -->
          <!-- <img class="dc-background" src="" alt="dc-background"> -->
          <!-- <div class="dc-background" alt="dc-background"> -->
        </div>
      </div>
    </div>

    <div class="container-bottom col align-items-center justify-content-center">
      <div class="container row justify-content-between">
        <button>SIGN-UP NOW!</button>
        <div class="container-bottom-right row align-items-center">
          <h3>FOLLOW US</h3>
          <ul class="d-flex">
            <li v-for="(linkFooterBottom, index) in linksFooterBottom" :key="index"><a :href="`${linkFooterBottom.url}`"><img :src="`${linkFooterBottom.img}`" :alt="`${linkFooterBottom.name}`"></a></li>
            <!-- <li><img src="../assets/img/footer-facebook.png" alt="img-footer-down"></li>
            <li><img src="../assets/img/footer-twitter.png" alt="img-footer-down"></li>
            <li><img src="../assets/img/footer-youtube.png" alt="img-footer-down"></li>
            <li><img src="../assets/img/footer-pinterest.png" alt="img-footer-down"></li>
            <li><img src="../assets/img/footer-periscope.png" alt="img-footer-down"></li> -->
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
    background-image: url('../assets/img/footer-bg.jpg');
    background-position: center;
    .big-container{
      height: 100%;
    }
    .half-container{

    }
    .half-container-left{
      padding: 30px 0;
      width: 40%;
    }
      .half-container-right{
      width: 60%;
      background-image: url('../assets/img/dc-logo-bg.png');
      background-position: center;
      background-repeat: no-repeat;
      position: relative;
      .dc-background{

      }
    }
    .col{
      padding: 0 10px;
    }
    ul{

      & *{
        color: $tertiary-color;
      }
      h4{
        padding: 10px 0;
        cursor: pointer;
      }
      li{
        padding: 5px 0;
        a{
          color: $quaternary-color;
          font-size: 12px;
          text-transform: capitalize;
          text-decoration: none;
          &:hover{
            cursor: pointer;
            color: $tertiary-color;
          }        
        }
      }
    }
  }

  .container-bottom{
    height: 100px;
    background-color: $quinary-color;

    .container-bottom-right{

      h3{
        color: $primary-color;
        cursor: pointer;
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
      &:hover{
        background-color: $tertiary-color;
        color: $primary-color;
      }
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