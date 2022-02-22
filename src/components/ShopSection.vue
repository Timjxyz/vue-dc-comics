<template>
  <section class="shop">
    <div class="container">
      <div  v-for="(link, index) in links" :key="index" class="img-shop">
        <img img :src="link.url"  alt="">
        <div class="img-text">{{link.text}}</div>
      </div>
     
    </div>
  </section>
</template>

<script>
export default {
  name: 'ShopSection',
  data() {
    return {
      links: [
          {
              text: "DIGITAL COMICS",
              url: require("../assets/img/buy-comics-digital-comics.png"),
              current: false,
          },
          {
              text: "DC-MERCHANDISE",
              url: require("../assets/img/buy-comics-merchandise.png"),
              current: true,
          },
          {
              text: "SUBSCRIPTION",
              url: require("../assets/img/buy-comics-subscriptions.png"),
              current: false,
          },
          {
              text: "COMIC SHOP LOCATOR",
              url:require( "../assets/img/buy-comics-shop-locator.png"),
              current: false,
          },
          {
              text: "DC POWER VISA",
              url: require("../assets/img/buy-dc-power-visa.svg"),
              current: false,
          },
        
      ],
    }

  }
 
}
</script>


<style scoped lang="scss">
@import "../assets/variables.scss";
.shop{
  background-color: $primaryColor;
  z-index: 1000;
  position: absolute;
  width: 100%;

  .container{
    display: flex;
    justify-content: space-around;
    align-items: center;
    min-height: 150px;

    .img-shop{
      display: flex;
      align-items: center;
      justify-content: space-around;

      img{
        height:50px;
        width: 50px;
        object-fit: contain;
        margin-right: 10px;    
      }

      .img-text{
        color:$colorWhite;
      }
    }

  }

}
</style>
