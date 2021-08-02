<template>
  <Header></Header>
  <Advantages></Advantages>
  <Slider></Slider>
  <Purchases></Purchases>
  <Footer></Footer>
</template>

<script>
import Header from './components/Header.vue'
import Advantages from './components/Advantages.vue'
import Slider from './components/Slider.vue'
import Purchases from './components/Purchases.vue'
import Footer from './components/Footer.vue'

export default {
  name: 'App',
  components: {
    Header,
    Advantages,
    Slider,
    Purchases,
    Footer
  }
}
</script>

<style>
body {
  margin: 0;
  padding: 0;
  font-family: 'Montserrat', sans-serif;
  background-color: #F6F6F6;
}
</style>
