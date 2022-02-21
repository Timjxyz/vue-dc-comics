<template>
  <main>
    <div class="container">
      <p>CONTENT GOES HERE</p>
    </div>

  </main>
</template>

<script>
export default {
  name: 'MyMain',
 
}
</script>


<style scoped lang="scss">
@import "../assets/variables.scss";
main{
  background-color: $backgMain;
  min-height: 150px;
  color: #fff;
  .container{
    height: 100%;
    padding-top: 50px;
    p{
      vertical-align: middle;
    }
  }
}
</style>
