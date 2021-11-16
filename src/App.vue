<template>
  <Header/>
  <Main/>
  <Specs/>
  <Managment/>
  <Customer/>
  <Collaborative/>
  <Quick/>
  <Strategies/>
  <Price/>
  <Clients/>
  <Banner/>
  <Footer/>
</template>

<script>
import Header from '@/components/Header.vue'
import Main from '@/components/Main.vue'
import Specs from '@/components/Specs.vue'
import Managment from '@/components/Managment.vue'
import Customer from '@/components/Customer.vue'
import Collaborative from '@/components/Collaborative.vue'
import Quick from '@/components/Quick.vue'
import Strategies from '@/components/Strategies.vue'
import Price from '@/components/Price.vue'
import Clients from '@/components/Clients.vue'
import Banner from '@/components/Banner.vue'
import Footer from '@/components/Footer.vue'

export default {
  components:{
Header, Main, Specs, Managment, Customer, Collaborative, Quick, Strategies, Price, Clients, Banner, Footer
  }
}
</script>

<style lang="scss">
@import './colors.scss';
@import url(https://fonts.googleapis.com/css?family=Roboto:100,100italic,300,300italic,regular,italic,500,500italic,700,700italic,900,900italic);
*{
  font-family: 'Roboto', sans-serif;
}
html,body, p,ul,ol,li, h1, h2, span{
  margin: 0;
  padding: 0;
}
/* ::-webkit-scrollbar {
  width: 0;
} */


</style>
