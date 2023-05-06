<script>
import {linksCta} from "../data/container-cta"

import data from "../data/dc-comics.json"
import Card from "../components/partials/Card.vue"
export default {
  name: 'Main',
  components:{
    Card
  },
  data(){
    return{
      linksCta,
      data,
    }
  }
}
</script>

<template>
  <body class="d-flex col justify-content-center align-items-center">
    <div class="container-content col justify-content-center align-items-center">

      <div class="container-100 col justify-content-center align-items-center">
        <div class="main-container-image container-100">
          <div class="current-series">CURRENT SERIES</div>
        </div>

        <div class="cards-container container row flex-wrap">

          <!-- * cards in maniera dinamica TRAMITE PROPS-->
          <!-- ! importa il componente card -->
          <Card
            v-for="(singleData, index) in data"
            :key="index"
            :imgSrc="singleData.thumb"
            :nameSerie="singleData.series" 
          />

          <!-- * cards in maniera dinamica-->
          <!-- <div v-for="(singleData, index) in data" :key="index" class="card col">
            <img :src="`${singleData.thumb}`" :alt="`${singleData.series}`">
            <div>{{ singleData.series }}</div>
          </div> -->

          <!-- * cards -->
          <!-- <div class="card col">
            <img src="../assets/img/jumbotron.jpg" alt="img-card">
            <div>ACTION COMICS</div>
          </div>

          <div class="card col">
            <img src="../assets/img/jumbotron.jpg" alt="img-card">
            <div>ACTION COMICS</div>
          </div>

          <div class="card col">
            <img src="../assets/img/jumbotron.jpg" alt="img-card">
            <div>ACTION COMICS</div>
          </div>

          <div class="card col">
            <img src="../assets/img/jumbotron.jpg" alt="img-card">
            <div>ACTION COMICS</div>
          </div>

          <div class="card col">
            <img src="../assets/img/jumbotron.jpg" alt="img-card">
            <div>ACTION COMICS</div>
          </div>

          <div class="card col">
            <img src="../assets/img/jumbotron.jpg" alt="img-card">
            <div>ACTION COMICS</div>
          </div>

          <div class="card col">
            <img src="../assets/img/jumbotron.jpg" alt="img-card">
            <div>ACTION COMICS</div>
          </div>

          <div class="card col">
            <img src="../assets/img/jumbotron.jpg" alt="img-card">
            <div>ACTION COMICS</div>
          </div>

          <div class="card col">
            <img src="../assets/img/jumbotron.jpg" alt="img-card">
            <div>ACTION COMICS</div>
          </div>

          <div class="card col">
            <img src="../assets/img/jumbotron.jpg" alt="img-card">
            <div>ACTION COMICS</div>
          </div>

          <div class="card col">
            <img src="../assets/img/jumbotron.jpg" alt="img-card">
            <div>ACTION COMICS</div>
          </div>

          <div class="card col">
            <img src="../assets/img/jumbotron.jpg" alt="img-card">
            <div>ACTION COMICS</div>
          </div>

          <div class="card col">
            <img src="../assets/img/jumbotron.jpg" alt="img-card">
            <div>ACTION COMICS</div>
          </div>

          <div class="card col">
            <img src="../assets/img/jumbotron.jpg" alt="img-card">
            <div>ACTION COMICS</div>
          </div> -->

        <div class="container-100 col justify-content-center align-items-center">
          <button class="load-more-btn">LOAD MORE</button>
        </div>
          
        </div>
      </div>
    </div>
    
    <div class="container-cta col justify-content-center align-items-center">
      <div class="container row align-items-center justify-content-around">
        <div v-for="(linkCta, index) in linksCta" :key="index" class="col">
        <a :href="`${linkCta.url}`">
          <div class="item-cta row align-items-center">
            <div class="col">
              <img :src="`${linkCta.img}`" :alt="`${linkCta.name}`">
            </div>
            <div class="col justify-content align-items-center">
              <div class="name-item">{{ linkCta.name }}</div>
            </div>
          </div>
        </a>
        </div>
        <!-- <div class="col">
          <div class="item-cta row align-items-center">
            <div class="col">
              <img src="../assets/img/buy-comics-digital-comics.png" alt="img">
            </div>
            <div class="col justify-content align-items-center">
              <div class="name-item">digital comics</div>
            </div>
          </div>
        </div>
        <div class="col">
          <div class="item-cta row align-items-center">
            <div class="col">
              <img src="src\assets\img\buy-comics-merchandise.png" alt="img">
            </div>
            <div class="col">
              <div class="name-item">dc merchandise</div>
            </div>
          </div>
        </div>
        <div class="col">
          <div class="item-cta row align-items-center">
            <div class="col">
              <img src="src\assets\img\buy-comics-subscriptions.png" alt="img">
            </div>
            <div class="col justify-content align-items-center">
              <div class="name-item">subscription</div>
            </div>
          </div>
        </div>
        <div class="col">
          <div class="item-cta row align-items-center">
            <div class="col">
              <img class="position-img" src="src\assets\img\buy-comics-shop-locator.png" alt="img">
            </div>
            <div class="col justify-content align-items-center">
              <div class="name-item">comic shop locator</div>
            </div>
          </div>
        </div>
        <div class="col">
          <div class="item-cta row align-items-center">
            <div class="col">
              <img class="visa-img" src="../assets/img/buy-dc-power-visa.svg" alt="img-visa">
            </div>
            <div class="col justify-content align-items-center">
              <div class="name-item">dc power visa</div>
            </div>
          </div>
        </div> -->
      </div>
    </div>
  
  </body>

</template>

<style lang="scss" scoped>
  @use '../scss/main.scss' as *;

  h1{
    color: $tertiary-color;
  }

  a{
    text-decoration: none;
  }

  body{
    .container-content{
      width: 100%;
      // height: 110px;
      background-color: $senary-color;

      .main-container-image{
        height: 400px;
        background-image: url('../assets/img/jumbotron.jpg');
        background-position: top;
        background-repeat: no-repeat;
        position: relative;
        .current-series{
          position: absolute;
          // bottom: -50px;
          // left: 180px;
          bottom: -25px;
          left: 10%;
          background-color: $primary-color;
          color: $tertiary-color;
          font-weight: 600;
          font-size: 27px;
          padding: 10px 25px;
        }
      }
      .cards-container{
        margin: 30px;

    //.card NON è PIU' NECESSARIO QUI IL CODICE è STATO SPOSTATO NE COMPONENTE CARD
        // .card{
        //   height: 230px;
        //   width: 180px;
        //   color: $tertiary-color;
        //   margin: 30px 10px;
        //   &:hover{
        //     color: $primary-color;
        //     cursor: pointer;
        //   }
        //   img{
        //     height: 180px;
        //     width: 180px;
        //     margin-bottom: 15px;
        //   }
        // }
        .load-more-btn{
          margin: 0 auto;
          background-color: $primary-color;
          cursor: pointer;
          overflow: hidden;
          outline: none;
          color: $tertiary-color;
          border: 3px $primary-color solid;
          font-size: 16px;
          padding: 5px 25px;
          font-weight: 600;
          &:hover{
            background-color: $tertiary-color;
            // color: $senary-color;
            color: $primary-color;
          }
        }
      }
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

  //per ridurre le dimensioni della 4 immagine nella barra azzurra
  .container-cta .container .col:nth-child(4) img {
      width: auto;
      height: 40px;
    }

  .item-cta{
    color: $tertiary-color;
    text-transform: uppercase;
    &:hover{
      text-decoration: underline;
    }
    img{
      width: 40px;
      margin-right: 8px;
      cursor: pointer;
      
    }
    
    //per ridurre le dimensioni della 4 immagine nella barra azzurra
    // .position-img{
    //   width: auto;
    //   height: 40px;
    // }

    .name-item{
      font-size: 14px;
      cursor: pointer;

    }
  }








</style>