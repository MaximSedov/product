<template>
  <section class='managment'>
    <el-row  justify='center' class='managment_content'>
      <el-col :xs='22' :sm='22' :md='10' :lg='7' :xl='7'>
        <div class='subtitle'>
          <span>Effortless Validation forас</span>
        </div>
        <div class="title">Управление</div>
        <div class="text">Lorem ipsum, dolor sit amet consectetur adipisicing elit. Ab culpa iure quaerat odit. Quo molestias odit tempora repellendus voluptas, omnis aperiam libero vero porro in doloribus obcaecati, excepturi possimus quasi.</div>
        <div class="subtitle">Lorem, ipsum dolor.</div>
        <div class="text">Lorem ipsum dolor sit, amet consectetur adipisicing elit. Corrupti est magnam vero quis necessitatibus, iusto labore rem fugit ut nesciunt, ipsam numquam adipisci sit, delectus officia praesentium atque quos accusamus.</div>
        <div class="subtitle">Lorem, ipsum dolor.</div>
        <div class="text">Lorem ipsum dolor sit amet consectetur, adipisicing elit. Esse sint rerum, molestiae assumenda odio soluta consequatur laudantium. Alias, veniam quidem.</div>
      </el-col>
      <el-col :xs='22' :sm='22' :md='10' :lg='13' :xl='13'>
        <div class='managment_content--img'>
          <el-image :src='managment' fit='cover' lazy></el-image>
        </div>
      </el-col>
    </el-row>
  </section>
</template>

<script>
const managment = require('../assets/managment.png')
export default {
  data() {
    return {
      managment
    }
  },
  components: {
    
  },
}
</script>

<style lang="scss">
@import '../colors.scss';
.managment {
  margin-top: 6rem;
  &_content {
    display: flex;
    justify-content: space-between;
    align-items: center;
    .subtitle{
      font-weight: bold;
      font-size: 1.1rem;
      margin-bottom: 1rem;
    }
    .title{
      font-size: 2rem;
      font-weight: bold;
      margin-bottom: 2rem;
    }
    .text{
      margin-bottom: 2rem;
    }
    &--img{
      display: flex;
      justify-content: end;
    }
    
  }
}
@media only screen and (max-width: 992px) {
  .managment_content--img{
    margin-top: 2rem;
    justify-content: center;
  }
}
</style>