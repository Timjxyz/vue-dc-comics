<template>
  <header>
    <div class="container">
      <!-- Logo della pagina -->
    <div class="logo">
      <img src="../assets/img/dc-logo.png" alt="">
    </div>
    <nav>
      <ul>
        <li>
          <a href="#"> CHARACTERS</a>
        </li>
         <li>
          <a href="#" class="active"> COMICS</a>
        </li>
         <li>
          <a href="#"> MOVIES</a>
        </li>
         <li>
          <a href="#"> TV</a>
        </li>
         <li>
          <a href="#"> GAMES</a>
        </li>
         <li>
          <a href="#"> COLLECTIBLES</a>
        </li>
         <li>
          <a href="#"> VIDEOS</a>
        </li>
         <li>
          <a href="#"> FANS</a>
        </li>
         <li>
          <a href="#"> NEWS</a>
        </li>
         <li>
          <a href="#"> SHOP</a>
        </li>
      </ul>
    </nav>

    </div>
  </header>
</template>

<script>
export default {
  name: 'MyHeader',
}
</script>


<style scoped lang="scss">
@import "../assets/variables.scss";

.container{
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  justify-content: space-between;
  height: 100px;
  margin-top: 20px;

  .logo{
    img{
      height: 70px;
    }
  }
}

nav{
  ul{
    display: flex;
    li{
      list-style: none;
      
      a{
        text-decoration: none;
        padding: 10px;
        font-size: 14px;
        color: $colorBlack;
        font-weight: 500;
        padding-bottom: 36px;
        &.active, &:hover{
          border-bottom: 5px solid $primaryColor;
            
        }
      }
    }
  }
}
</style>
