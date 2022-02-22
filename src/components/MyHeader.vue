<template>
  <header>
    <div class="container">
      <!-- Logo della pagina -->
    <div class="logo">
      <img src="../assets/img/dc-logo.png" alt="">
    </div>
    <nav>

      <ul>
        <li v-for="(link, index) in links" :key="index" >
          <a :class="link.current?'active':''" :href="link.url"> {{link.text}}</a>
        </li>
        
      </ul>
    </nav>

    </div>
  </header>
</template>

<script>
export default {
  name: 'MyHeader',
  data() {
    return {
      links: [
              {
                  text: "CHARACTERS",
                  url: "#",
                  current: false,
              },
              {
                  text: "COMICS",
                  url: "#",
                  current: true,
              },
              {
                  text: "MOVIES",
                  url: "#",
                  current: false,
              },
              {
                  text: "TV",
                  url: "#",
                  current: false,
              },
              {
                  text: "GAMES",
                  url: "#",
                  current: false,
              },
              {
                  text: "COLLECTIBLES",
                  url: "#",
                  current: false,
              },
              {
                  text: "VIDEOS",
                  url: "#",
                  current: false,
              },
              {
                  text: "FANS",
                  url: "#",
                  current: false,
              },
              {
                  text: "NEWS",
                  url: "#",
                  current: false,
              },
              {
                  text: "VIDEOS",
                  url: "SHOP",
                  current: false,
              },
      ],
    }

  }
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
