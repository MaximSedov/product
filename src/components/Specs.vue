<template>
  <section class='specs' id="specs">
    <el-row  justify='center' class='specs_content'>
      <el-col :xs='22' :sm='22' :md='8' :lg='20' :xl='20'>
        <div class='header'>
          <h2>Продукт был создан специально для Вас</h2>
        </div>
      </el-col>
    </el-row>
    <el-row  justify='center' class='specs_content'>
      <el-col v-for='(item, index) in specs' :key='item.index' :xs='11' :sm='11' :md='5' :lg='5' :xl='5' class='specs_content--items'>
        <div class='item'>
          <div class='item-icon'>
            <Icon size='24'>
              <component :is='item.icon'></component>
            </Icon>
          </div>
          <div class='item-title'>{{item.title}}</div>
          <div class='item-text'>{{item.text}}</div>
        </div>
      </el-col>
    </el-row>
    <el-row  justify='center'>
      <el-col :xs='12' :sm='12' :md='10' :lg='10' :xl='10' style="text-align: center; margin-top: 3rem; margin-bottom:3rem;">
         <el-button style="font-weight:bold" type='success'>Присоединиться сейчас</el-button>
      </el-col>
    </el-row>
  </section>
</template>

<script>
import {
  CursorClick24Filled,
  Lottery24Filled,
  Heart16Filled,
  Smartwatch20Filled,
} from '@vicons/fluent'
import { Icon } from '@vicons/utils'

export default {
  data() {
    return {
      specs: [
        {
          title: 'Фича 1',
          text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Veniam, totam?',
          icon: 'CursorClick24Filled',
        },
        {
          title: 'Фича 2',
          text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Veniam, totam?',
          icon: 'Lottery24Filled',
        },
        {
          title: 'Фича 3',
          text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Veniam, totam?',
          icon: 'Heart16Filled',
        },
        {
          title: 'Фича 4',
          text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Veniam, totam?',
          icon: 'Smartwatch20Filled',
        },
      ],
    }
  },
  components: {
    Icon,
    CursorClick24Filled,
    Lottery24Filled,
    Heart16Filled,
    Smartwatch20Filled,
  },
}
</script>

<style lang="scss">
@import '../colors.scss';
.specs {
  
  &_content {
    padding-top: 1rem;
    display: flex;
    justify-content: space-between;
    align-items: center;
    .header {
      text-align: center;
      margin-bottom: 3rem;
      margin-top: 3rem;
      h2 {
        font-size: 2rem;
        color: var(--text-primary-color) !important;
      }
    }
    &--items {
      .item {
        &-icon {
          .xicon {
            padding: 0.5rem;
            border-radius: 1rem;
            color: var(--background-color-primary);
          }
        }
        &-title {
          margin-top: 1rem;
          margin-bottom: 1rem;
          font-weight: bold;
          font-size: 1.3rem;
          color: var(--text-primary-color);
        }
        &-text{
          color: var(--text-primary-color);
          padding-right: 1rem;
        }
      }
      &:nth-child(1) .xicon {
        background-color: $mainGreen;
      }
      &:nth-child(2) .xicon {
        background-color: $mainYellow;
      }
      &:nth-child(3) .xicon {
        background-color: $mainBlue;
      }
      &:nth-child(4) .xicon {
        background-color: $mainRed;
      }
    }
  }
}
@media only screen and (max-width: 992px) {
  .specs_content--items{
    .item{
      margin-bottom: 1rem;
    }
  }
}
</style>