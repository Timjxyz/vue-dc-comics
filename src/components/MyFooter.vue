<template>
  <footer>
    <!-- Parte superiore del footer -->
    <div class="footer-top clearfloat">
      <div class="container">
        <nav>
          <ul>
            <li>
              <h3>DC COMICS</h3>
            </li>

            <li>
              <a href="#"> characters</a>
            </li>
            <li>
              <a href="#" class="active"> comics</a>
            </li>
            <li>
              <a href="#"> movies</a>
            </li>
            <li>
              <a href="#"> tv</a>
            </li>
            <li>
              <a href="#"> games</a>
            </li>
            <li>
              <a href="#"> collectibles</a>
            </li>
            <li>
              <a href="#"> videos</a>
            </li>
            <li>
              <a href="#"> fans</a>
            </li>
            <li>
              <a href="#"> news</a>
            </li>
            <li>
              <a href="#"> shop</a>
            </li>
          </ul>
          <ul>
            <!-- secondo -->
             <li>
              <h3>DC COMICS</h3>
            </li>

            <li>
              <a href="#"> characters</a>
            </li>
            <li>
              <a href="#" class="active"> comics</a>
            </li>
             <li>
              <a href="#"> videos</a>
            </li>
            <li>
              <a href="#"> fans</a>
            </li>
            <li>
              <a href="#"> news</a>
            </li>
            <li>
              <a href="#"> shop</a>
            </li>
             <li>
              <a href="#"> videos</a>
            </li>
            <li>
              <a href="#"> fans</a>
            </li>
            <li>
              <a href="#"> news</a>
            </li>
            <li>
              <a href="#"> shop</a>
            </li>
             <li>
              <a href="#"> videos</a>
            </li>
            <li>
              <a href="#"> fans</a>
            </li>
            <li>
              <a href="#"> news</a>
            </li>
            <li>
              <a href="#"> shop</a>
            </li>
          </ul>

          <!-- terzo -->
          <ul>
             <li>
              <h3>DC COMICS</h3>
            </li>

            <li>
              <a href="#"> characters</a>
            </li>
            <li>
              <a href="#" class="active"> comics</a>
            </li>
             <li>
              <a href="#"> videos</a>
            </li>
          </ul>
           <!-- quarto -->
          <ul>
             <li>
              <h3>DC COMICS</h3>
            </li>

            <li>
              <a href="#"> characters</a>
            </li>
            <li>
              <a href="#" class="active"> comics</a>
            </li>
             <li>
              <a href="#"> videos</a>
            </li>
          </ul>
        </nav>

        <div class="bg-footer">
          <img src="../assets/img/dc-logo-bg.png" alt="">
        </div>
      </div>
    </div>

    <!-- Parte inferiore del footer -->
    <div class="footer-bottom clearfloat">
      <div class="container">

        <div class="button-footer">
          <button>SIGN-UP NOW</button>
        </div>
        
        <div class="social-footer">
              <a href="#"> FOLLOW US</a>
            <div class="img-social-footer"  v-for="(link, index) in links" :key="index">
              <img src="../assets/img/footer-facebook.png" alt="">
              
            </div>
            
            
        </div>
      </div>
    </div>

  </footer>

</template>

<script>
export default {
  name: 'MyFooter',
  data() {
    return {
      links: [
          {
             
              url: "../assets/img/footer-facebook.png",
              current: false,
          },
          {
              
              url: "../assets/img/footer-twitter.png",
              current: true,
          },
          {
              
              url: "../assets/img/footer-youtube.png",
              current: false,
          },
          {
              
              url: "../assets/img/footer-pinterest.png",
              current: false,
          },
          {
              
              url: "../assets/img/footer-periscope.png",
              current: false,
          },
        
      ],
    }

  }
 
}
</script>


<style scoped lang="scss">
@import "../assets/variables.scss";
footer{
  .footer-top{
    position: relative;
    background-image: url("../assets/img/footer-bg.jpg");
    background-repeat: no-repeat;
    background-size: cover;
    margin-top: 150px;
    .container{
      
      display: flex;
      justify-content: space-around;
      nav{
        padding-top: 50px;
        float: left;
        display: flex;
        width: 30%;
        flex-wrap: wrap;
        justify-content: space-between;
        ul{
          li{
            list-style: none;
      
            h3{
              color:$colorWhite;
              margin-bottom: 10px;
            }
            a{
              text-decoration: none;
              color: gray;
              text-transform: capitalize;
              font-size: 12px;
            }
          }
        }
      }
      .bg-footer{
        width: 50%;
        float: right;
        img{
          position: absolute;
          bottom :-40px;
        }
      }

    }
    .clearfloat{
      display: table;
      clear: both;
      content: "";
    }
  }
  //Regole footer-bottom
  .footer-bottom{
    background-color:$colorFooterBottom;
    z-index: 10;
    position: absolute;
    width: 100%;
    
    .container{
      display: flex;
      vertical-align: middle;
      .button-footer{
        float: left;
        width: 50%;
        display: flex;
        align-items: center;

        button{
          background-color: $colorFooterBottom;
          border: 1px solid $primaryColor;
          padding: 10px;
          color:$colorWhite;
          font-weight: 600;
          &:hover{
            cursor: pointer;
          }
        }
        
      }
      .social-footer{
        float: right;
        width: 50%;
        text-align: center;
        display: flex;
        align-items: center;
         
          a{
            text-decoration: none;
            color: $primaryColor;
            font-weight: 600;
          }
        .img-social-footer{
          display: flex;
          align-items: center;
          img{
            margin: 20px;
          }
        }
      }
    }
    .clearfloat{
      display: table;
      clear: both;
      content: "";
    }
  }
}
</style>
