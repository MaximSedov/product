<template>
  
  <Header/>
  <Main/>
  <Specs/>
  <Managment/>
</template>

<script>
import Header from '@/components/Header.vue'
import Main from '@/components/Main.vue'
import Specs from '@/components/Specs.vue'
import Managment from '@/components/Managment.vue'
export default {
  components:{
Header, Main, Specs, Managment
  }
}
</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Noto+Sans+Mono:wght@100;200;300;400;500;700;800;900&display=swap');
*{
  font-family: 'Noto Sans Mono', monospace;
}
body,p,ul,li, h1, h2, span{
  margin: 0;
  padding: 0;
}



</style>
