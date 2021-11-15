<template>
  <section class='main'>
    <el-row :gutter='10' justify='center' class='main_content'>
      <el-col :xs='8' :sm='6' :md='4' :lg='8' :xl='8'>
        <div class='main_content--text'>
          <div class='header'> <h1>Работайте со скоростью мысли</h1> </div>
          <div class='text'>
            <p>Инструменты, уроки, эксперты по дизайну и инновациям - все в одном месте! Лучший интуитивно понятный способ представить ваш следующий пользовательский опыт.</p>
          </div>
          <div class='buttons'>
            <el-button type='success'>Начать</el-button>
            <Icon size='24'>
              <PlayArrowRound />
            </Icon>
            <span class="watch_button">Посмотреть видео</span>
          </div>
        </div>
        <div class='main_content--img'></div>
      </el-col>
      <el-col :xs='8' :sm='6' :md='4' :lg='12' :xl='12'>
        <div class='main_content--img'>
          <el-image :src='main' fit='cover'></el-image>
        </div>
      </el-col>
    </el-row>
  </section>
</template>

<script>
import { PlayArrowRound } from '@vicons/material'
import { Icon } from '@vicons/utils'
const main = require('../assets/main.png')
export default {
  data() {
    return {
      main,
    }
  },
  components: {
    Icon,
    PlayArrowRound,
  },
}
</script>

<style lang="scss">
@import '../colors.scss';
.main {
  background-image: url('../assets/main-bg.png');
  background-repeat: no-repeat;
  background-size: cover;
  background-position-x: center;
  background-position-y: top;
  min-height: 800px;
  display: flex;
  align-items: center;
  &_content {
    padding-top: 2rem;
    display: flex;
    justify-content: space-between;
    align-items: center;
    &--text {
      .header {
        h1{
          font-size: 3rem;
        font-weight: bold;
        margin-bottom: 2rem;
        line-height: 3.5rem;
        color: $mainBlack;
        }
        
      }
      .text{
        margin-bottom: 2rem;
        p{
          font-weight: 500;
        }
        
      }
      .buttons{
        display: flex;
        align-items: center;
        
        .el-button{
          margin-right: 2rem;
          font-weight: bold;
        }
        .xicon{
          color: $mainGreen;
        }
        .watch_button{
          color: $mainGreen;
          text-decoration: underline;
          &:hover{
            cursor: pointer;
            color: $lightGreen;
          }
        }
      }
    }
    &--img {
      display: flex;
      justify-content: end;
    }
  }
}
</style>