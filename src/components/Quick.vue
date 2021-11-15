<template>
  <section class='quick'>
    <el-row :gutter='10' justify='center' class='quick_content'>
      <el-col :xs='8' :sm='6' :md='4' :lg='20' :xl='20'>
        <div class='header'>
          <h2>Быстрый и легкий процесс</h2>
        </div>
      </el-col>
    </el-row>
    <el-row :gutter='10' justify='center' class='quick_content'>
      <el-col v-for='(item, index) in quick' :key='item.index' :xs='12' :sm='12' :md='5' :lg='5' :xl='5' class='quick_content--items'>
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
    <el-row :gutter='10' justify='center'>
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
      quick: [
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
.quick {
  
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
        color: $mainBlack !important;
      }
    }
    &--items {
      .item {
        &-icon {
          .xicon {
            padding: 0.5rem;
            border-radius: 1rem;
            color: $white;
          }
        }
        &-title {
          margin-top: 1rem;
          margin-bottom: 1rem;
          font-weight: bold;
          font-size: 1.3rem;
          color: $mainBlack;
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
</style>