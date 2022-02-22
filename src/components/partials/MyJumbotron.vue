<template>
  <div class="img-container">
      <img :src="require('../../assets/img/jumbotron.jpg')">
  </div>
</template>

<script>
export default {
name:'MyJumbotron'
}
</script>

<style scoped lang="scss">
.img-container{
    height: 300px;
    text-align: center;
    img{
        width: 100%;
        height: 100%;
        object-fit: cover;
        
        
    }
}

</style>