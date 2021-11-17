<template>
  <section class='header'>
    <el-row justify='center'>
      <el-col :xs='22' :sm='22' :md='20' :lg='20' :xl='20'>
        <div class='header_content'>
          <div class='header_content--logo'>
            <el-image style='width: 60px; height: 60px' :src='logo' fit='cover'></el-image>Product
          </div>
          <div class='header_content--navbar'>
            <div class='header_content--navbar__links desktop'>
              <div class v-for='(item, index) in navbar' :key='item.index'>{{item.title}}</div>
            </div>
            <div class='header_content--navbar__links mobile-md'>
              <el-button style='padding: 0 10px;margin-right: 2rem;' type='success' @click="drawer = true">
                <Icon size='24'>
                  <MenuIcon />
                </Icon>
              </el-button>
            </div>
            <div class='header_content--navbar__buttons mobile-xs'>
              <el-button class='signin'>Вход</el-button>
              <el-button style='margin-right:2rem' type='success'>Регистрация</el-button>
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
    <el-drawer v-model='drawer' title='Меню' direction='ttb' size="100%">
      <div class="header_content--navbar__links--mobile">
         <div class v-for='(item, index) in navbar' :key='item.index'>{{item.title}}</div>
      </div>
    </el-drawer>
  </section>
</template>

<script>
import ModeNightRound from '@vicons/material/ModeNightRound'
import MenuIcon from '@vicons/tabler/Menu'
import { Icon } from '@vicons/utils'
const logo = require('../assets/cubes.png')
export default {
  data() {
    return {
      logo,
      drawer: false,
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
    MenuIcon,
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
      color: $mainBlack;
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
        .signin {
          &:hover,
          &:active,
          &:focus {
            background-color: $lightGreenOpacity !important;
            color: $white !important;
            border-color: $lightGreenOpacity !important;
          }
        }
      }
      &__nightmode {
        display: flex;
        align-items: center;
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
  &_content--navbar__links--mobile{
    text-align: center;
    color: $mainBlack;
    div{
      font-size: 1.5rem;
      margin-bottom: 1rem;
      &:hover{
        color: $mainGreen;
        cursor: pointer;
      }
    }
  }
}
@media only screen and (min-width: 992px) {
  .mobile-md {
    display: none;
  }
}
@media only screen and (max-width: 992px) {
  .desktop {
    display: none;
  }
}
@media only screen and (max-width: 768px) {
  .mobile-xs {
    display: none;
  }
}
</style>