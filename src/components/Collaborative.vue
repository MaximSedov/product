<template>
  <section class='collaborative'>
    <el-row justify='center' class='collaborative_content'>
      <el-col :xs='22' :sm='22' :md='10' :lg='7' :xl='7'>
        <div class='subtitle'>
          <span>Lorem, ipsum dolor.</span>
        </div>
        <div class="title">Совместно</div>
        <div class="text">Lorem ipsum, dolor sit amet consectetur adipisicing elit. Ab culpa iure quaerat odit. Quo molestias odit tempora repellendus voluptas, omnis aperiam libero vero porro in</div>
        <div class="subtitle">Lorem, ipsum dolor.</div>
        <div class="text">Lorem ipsum dolor sit, amet consectetur adipisicing elit. Corrupti est magnam vero quis necessitatibus, iusto labore rem fugit ut nesciunt, ipsam numquam adipisci</div>
        <div class="subtitle">Lorem, ipsum dolor.</div>
        <div class="text">Lorem ipsum dolor sit amet consectetur, adipisicing elit. Esse sint rerum, molestiae assumenda odio soluta consequatur laudantium. Alias, veniam quidem.</div>
      </el-col>
      <el-col :xs='22' :sm='22' :md='10' :lg='13' :xl='13'>
        <div class='collaborative_content--img'>
          <el-image :src='collaborative' fit='cover' lazy></el-image>
        </div>
      </el-col>
    </el-row>
  </section>
</template>

<script>
const collaborative = require('../assets/collaborative.png')
export default {
  data() {
    return {
      collaborative
    }
  },
  components: {
    
  },
}
</script>

<style lang="scss">
@import '../colors.scss';
.collaborative {
  margin-top: 6rem;
  &_content {
    display: flex;
    justify-content: space-between;
    align-items: center;
    .subtitle{
      font-weight: bold;
      font-size: 1.1rem;
      margin-bottom: 1rem;
      color: var(--text-primary-color);
    }
    .title{
      font-size: 2rem;
      font-weight: bold;
      margin-bottom: 2rem;
      color: var(--text-primary-color);
    }
    .text{
      margin-bottom: 2rem;
      color: var(--text-primary-color);
    }
    &--img{
      display: flex;
      justify-content: end;
    }
    
  }
}
@media only screen and (max-width: 992px) {
  .collaborative_content--img{
    margin-top: 2rem;
    justify-content: center;
  }
}
</style>