<template>
  <div id="app">
    <MyHeader></MyHeader>
    <MyMain></MyMain>
    <ShopSection></ShopSection>
    <MyFooter></MyFooter>
  </div>
</template>

<script>
import MyHeader from './components/MyHeader.vue'
import MyMain from './components/MyMain.vue'
import ShopSection from './components/ShopSection.vue'
import MyFooter from './components/MyFooter.vue'


export default {
  name: 'App',
  components: {
    MyHeader,
    MyMain,
    ShopSection,
    MyFooter
  }
}
</script>

<style lang="scss">
@import "./assets/general.scss"
</style>
