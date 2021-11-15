<template>
  <section class='header'>
    <el-row :gutter='10' justify='center'>
      <el-col :xs='8' :sm='6' :md='4' :lg='20' :xl='20'>
        <div class='header_content'>
          <div class='header_content--logo'>
            <el-image style='width: 60px; height: 60px' :src='logo' fit='cover'></el-image>Product
          </div>
          <div class='header_content--navbar'>
            <div class='header_content--navbar__links'>
              <div class v-for='(item, index) in navbar' :key='item.index'>{{item.title}}</div>
            </div>
            <div class='header_content--navbar__buttons'>
              <el-button>Вход</el-button>
              <el-button type='success'>Регистрация</el-button>
            </div>
            <div class='header_content--navbar__nightmode'>
              <Icon size='24'>
                <ModeNightRound />
              </Icon>
            </div>
          </div>
        </div>
      </el-col>
    </el-row>
  </section>
</template>

<script>
import { ModeNightRound } from '@vicons/material'
import { Icon } from '@vicons/utils'
const logo = require('../assets/cubes.png')
export default {
  data() {
    return {
      logo,
      navbar: [
        { title: 'Продукт' },
        { title: 'Клиенты' },
        { title: 'Цены' },
        { title: 'Контакты' },
      ],
    }
  },
  components: {
    Icon,
    ModeNightRound,
  },
}
</script>

<style lang="scss">
@import '../colors.scss';
.header {
  &_content {
    display: flex;
    justify-content: space-between;
    align-items: center;
    height: 80px;
    &--logo {
      display: flex;
      align-items: center;
      font-weight: bold;
      font-size: 1.5rem;
      .el-image {
        margin-right: 1rem;
      }
    }
    &--navbar {
      display: flex;
      justify-content: space-between;
      align-items: center;
      &__links {
        display: flex;
        div {
          box-sizing: border-box;
          margin-right: 2rem;
        }
        div:hover {
          color: $mainGreen;
          cursor: pointer;
        }
      }
      &__buttons {
      }
      &__nightmode {
        display: flex;
        align-items: center;
        margin-left: 2rem;
        background-color: $mainGray;
        padding: 0.5rem;
        border-radius: 50%;
        .xicon {
          color: $mainGreen;
        }
        &:hover {
          cursor: pointer;
          .xicon {
            color: $darkGreen;
          }
        }
      }
    }
  }
}
</style>