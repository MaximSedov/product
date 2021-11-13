<template>
  <section class='managment'>
    <el-row :gutter='10' justify='center' class='managment_content'>
      <el-col :xs='8' :sm='6' :md='10' :lg='10' :xl='10'>
        <div class='header'>
          <h2>Продукт был создан специально для Вас</h2>
        </div>
      </el-col>
      <el-col :xs='8' :sm='6' :md='10' :lg='10' :xl='10'>
        <div class='header'>
          <h2>Продукт был создан специально для Вас</h2>
        </div>
      </el-col>
    </el-row>
  </section>
</template>

<script>

export default {
  data() {
    return {
      
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
    
  }
}
</style>