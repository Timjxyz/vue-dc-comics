<template>
  <div class="item">
        <img :src="src" :alt="titolo">
        <h3>{{titolo}}</h3>
        <h1>{{pippo}}</h1>
    </div>
</template>

<script>
 export default {
        name: 'MainItems',
        props: {
            "titolo": String, 
            "src": String
        },
       
    }
</script>

<style scoped lang="scss">
 @import "../../assets/variables.scss";
    .item {
        width:calc(100% / 6 - 20px);
        margin: 10px;
        h3 {
            margin-top: 10px;
            text-align: center;
            color: $colorWhite;
            font-size: 18px;
        }
        img {
            width: 100%;
           
        }
    }
    
</style>