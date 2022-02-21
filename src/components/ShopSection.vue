<template>
  <section class="shop">
    <div class="container">
      <div  v-for="(link, index) in links" :key="index" class="img-shop">
        <img src="../assets/img/buy-comics-digital-comics.png" alt="">
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
              url: "-comics-digital-comics.png",
              current: false,
          },
          {
              text: "DC-MERCHANDISE",
              url: "-comics-merchandise.png",
              current: true,
          },
          {
              text: "SUBSCRIPTION",
              url: "-comics-subscriptions.png",
              current: false,
          },
          {
              text: "COMIC SHOP LOCATOR",
              url: "-comics-shop-locator.png",
              current: false,
          },
          {
              text: "DC POWER VISA",
              url: "-dc-power-visa.svg",
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
        width: 50px;
         justify-content: space-around;
         object-fit: contain;
      }

      .img-text{
        color:$colorWhite;
      }
    }

  }

}
</style>
