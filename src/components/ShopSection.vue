<template>
  <section class="shop">
    <div class="container">
      <div class="img-shop">
        <img src="../assets/img/buy-comics-digital-comics.png" alt="">
        <div class="img-text">Digital comics</div>
      </div>
      <div class="img-shop">
        <img src="../assets/img/buy-comics-digital-comics.png" alt="">
        <div class="img-text">Digital comics</div>
      </div>
      <div class="img-shop">
        <img src="../assets/img/buy-comics-digital-comics.png" alt="">
        <div class="img-text">Digital comics</div>
      </div>
      <div class="img-shop">
        <img src="../assets/img/buy-comics-digital-comics.png" alt="">
        <div class="img-text">Digital comics</div>
      </div>
      <div class="img-shop">
        <img src="../assets/img/buy-comics-digital-comics.png" alt="">
        <div class="img-text">Digital comics</div>
      </div>

    </div>
  </section>
</template>

<script>
export default {
  name: 'ShopSection',
 
}
</script>


<style scoped lang="scss">
@import "../assets/variables.scss";
.shop{
  background-color: $primaryColor;

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
      }
      
      .img-text{
        color:$colorWhite;
      }
    }

  }

}
</style>
