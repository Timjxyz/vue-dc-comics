<template>
  <footer>
    <!-- Parte superiore del footer -->
    <div class="footer-top clearfloat">
      <div class="container">
        <div class="nav-footer">

         <FooterNav title="DC COMICS" :items="menuDcComics"/>
         <FooterNav title="DC" :items="dc"/>
         <FooterNav title="SITE" :items="sites"/>
         <FooterNav title="Shop" :items="shop"/>
        </div>




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
              <img img :src="link.url"  alt="">
              
            </div>
            
            
        </div>
      </div>
    </div>

  </footer>

</template>

<script>
import FooterNav from './partials/FooterNav.vue';
export default {
  name: 'MyFooter',
  components: {
    FooterNav
  },
  data() {
    return {
      links: [
          {
             
              url:require( "../assets/img/footer-facebook.png"),
              current: false,
          },
          {
              
              url: require("../assets/img/footer-twitter.png"),
              current: true,
          },
          {
              
              url: require("../assets/img/footer-youtube.png"),
              current: false,
          },
          {
              
              url: require("../assets/img/footer-pinterest.png"),
              current: false,
          },
          {
              
              url: require("../assets/img/footer-periscope.png"),
              current: false,
          },
        
      ],
 
      menuDcComics: [
        {
          src: "#",
          text: "Characters"
        },
        {
          src: "#",
          text: "Comics"
        },
        {
          src: "#",
          text: "Movies"
        },
        {
          src: "#",
          text: "TV"
        },
        {
          src: "#",
          text: "Games"
        },
        {
          src: "#",
          text: "Videos"
        },
        {
          src: "#",
          text: "News"
        }
      ],
      dc: [
        {
          src: "#",
          text: "Terms Of Use"
        },
        {
          src: "#",
          text: "Privacy policy (New)"
        },
        {
          src: "#",
          text: "Ad Choices"
        },
        {
          src: "#",
          text: "Advertising"
        },
        {
          src: "#",
          text: "jobs"
        },
        {
          src: "#",
          text: "Subscrition"
        },
        {
          src: "#",
          text: "Talent Workshops"
        },
        {
          src: "#",
          text: "CPSC Certificates"
        },
        {
          src: "#",
          text: "Rating"
        },
        {
          src: "#",
          text: "Shop Help"
        },
        {
          src: "#",
          text: "Contact Us"
        },
        
      ],
      sites: [
        {
          src: "#",
          text: "DC"
        },
        {
          src: "#",
          text: "MAD Magazine"
        },
        {
          src: "#",
          text: "DC Kids"
        },
        {
          src: "#",
          text: "DC Universe"
        },
        {
          src: "#",
          text: "DC Power Visa"
        },
        
      ],
      shop: [
        {
          src: "#",
          text: "Shop DC"
        },
        {
          src: "#",
          text: "Shop DC Collectibles"
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

      .nav-footer{
        float: left;
        width: 33%;
        padding-top: 20px;
        display: flex;
   
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
