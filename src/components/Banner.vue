<template>
  <section class='banner'>
    <el-row justify='center'>
      <el-col :xs='22' :sm='22' :md='18' :lg='18' :xl='18' class='banner_content'>
        <div class='text'>
          Присоединяйтесь к более чем
          <br />100 компаниям, которые улучшили
          <br />свой бизнес благодаря
          <br />нашему Продукту
        </div>
        <el-button type='success'>Купить сейчас</el-button>
      </el-col>
    </el-row>
  </section>
</template>

<script>
export default {
  data() {
    return {}
  },
  components: {},
}
</script>

<style lang="scss">
@import '../colors.scss';
.banner {
  margin-top: 6rem;
  &_content {
    min-height: 345px;
    background-color: $mainGreen;
    border-radius: 1rem;
    color: $white;
    background-image: url('../assets/screen.png');
    background-repeat: no-repeat;
    background-size: contain;
    background-position-x: right;
    background-position-y: center;
    .text {
      margin: 3rem;
      font-size: 2rem;
      font-weight: bold;
      line-height: 2.5rem;
    }
    .el-button {
      font-weight: bold;
      margin-bottom: 2rem;
      margin-top: 1rem;
      background-color: $white;
      color: $mainGreen;
      margin-left: 3rem;
      font-size: 1.5rem;
    }
  }
}
@media only screen and (max-width: 992px) {
  .banner_content{
    background-image: none;
  }
}
</style>