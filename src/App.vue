<template>
  <Header/>
  <Main/>
  <Specs/>
  <Managment/>
  <Customer/>
  <Collaborative/>
  <Quick/>
</template>

<script>
import Header from '@/components/Header.vue'
import Main from '@/components/Main.vue'
import Specs from '@/components/Specs.vue'
import Managment from '@/components/Managment.vue'
import Customer from '@/components/Customer.vue'
import Collaborative from '@/components/Collaborative.vue'
import Quick from '@/components/Quick.vue'

export default {
  components:{
Header, Main, Specs, Managment, Customer, Collaborative, Quick
  }
}
</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Noto+Sans+Mono:wght@100;200;300;400;500;700;800;900&display=swap');
*{
  font-family: 'Noto Sans Mono', monospace;
}
html,body, p,ul,li, h1, h2, span{
  margin: 0;
  padding: 0;
}
/* ::-webkit-scrollbar {
  width: 0;
} */


</style>
