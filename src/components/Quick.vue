<template>
  <section class='quick' id="quick">
    <el-row  justify='center' class='quick_content'>
      <el-col :xs='22' :sm='22' :md='20' :lg='20' :xl='20'>
        <div class='header'>
          <h2>Быстрый и легкий процесс</h2>
          <span>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Recusandae!</span>
        </div>
      </el-col>
      <el-col :xs='22' :sm='22' :md='10' :lg='8' :xl='8' class='quick_content--items mobile-reverse'>
        <div class='item'>
          <div class='avatar'>
            <el-avatar fit='contain' :size='100' :src='avatar_1'></el-avatar>
          </div>
          <div class='comment'>
            <span>Lorem, ipsum dolor.</span>
            <div class='comment--arrow_left'></div>
          </div>
        </div>
        <div class='item'>
          <div class='comment'>
            <span>Lorem, ipsum dolor.</span>
            <div class='comment--arrow_right'></div>
          </div>
          <div class='avatar'>
            <el-avatar fit='contain' :size='100' :src='avatar_2'></el-avatar>
          </div>
        </div>
      </el-col>
      <el-col :xs='22' :sm='22' :md='10' :lg='8' :xl='8' class='quick_content--items mobile'>
        <div class='item'>
          <div class='comment'>
            <span>Lorem, ipsum dolor.</span>
            <div class='comment--arrow_right'></div>
          </div>
          <div class='avatar'>
            <el-avatar fit='contain' :size='100' :src='avatar_3'></el-avatar>
          </div>
        </div>
        <div class='item'>
          <div class='avatar'>
            <el-avatar fit='contain' :size='100' :src='avatar_4'></el-avatar>
          </div>
          <div class='comment'>
            <span>Lorem, ipsum dolor.</span>
            <div class='comment--arrow_left'></div>
          </div>
        </div>
      </el-col>

      <el-col :xs='24' :sm='24' :md='20' :lg='20' :xl='20' style='text-align: center; margin-top: 3rem; margin-bottom:3rem;'>
        <el-button style='font-weight:bold' type='success'>Свяжитесь с нашим экспертом</el-button>
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
const avatar_1 = require('../assets/avatar-1.jpg')
const avatar_2 = require('../assets/avatar-2.jpg')
const avatar_3 = require('../assets/avatar-3.jpg')
const avatar_4 = require('../assets/avatar-4.jpg')
export default {
  data() {
    return {
      avatar_1,
      avatar_2,
      avatar_3,
      avatar_4,
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
  background-image: url('../assets/quick-bg.png');
  background-repeat: no-repeat;
  background-size: cover;
  background-position-x: center;
  background-position-y: bottom;
  min-height: 600px;

  &_content {
    min-height: 600px;
    padding-top: 1rem;
    display: flex;
    justify-content: space-between;
    align-items: center;
    align-content: center;
    .header {
      text-align: center;
      margin-top: 3rem;
      margin-bottom: 3rem;
      h2 {
        font-size: 2rem;
        color: var(--text-primary-color) !important;
        margin-bottom: 1rem;
      }
      span{
        color: var(--text-primary-color);
      }
    }
    &--items {
      display: flex;
      justify-content: center;
      .item {
        margin-bottom: 2rem;
        display: flex;
        align-items: center;
        justify-content: center;
        .avatar {
          margin-right: 2rem;
          margin-left: 2rem;
          .el-avatar--circle {
            border: 2px solid $darkGray;
          }
        }
        .comment {
          position: relative;
          background-color: var(--background-color-primary);
          border-radius: 2rem;
          padding: 1rem;
          z-index: 1;
          -webkit-box-shadow: 0px 5px 10px 2px rgba(34, 60, 80, 0.2);
          -moz-box-shadow: 0px 5px 10px 2px rgba(34, 60, 80, 0.2);
          box-shadow: 0px 5px 10px 2px rgba(34, 60, 80, 0.2);
          span {
            position: relative;
            z-index: 1000 !important;
            color: var(--text-primary-color);
          }
          &--arrow_left {
            position: absolute;
            width: 2rem;
            height: 2rem;
            border-radius: 0.5rem;
            background-color: var(--background-color-primary);
            left: 3rem;
            bottom: -0.5rem;
            transform: rotate(150deg);
            z-index: 1;
          }
          &--arrow_right {
            position: absolute;
            width: 2rem;
            height: 2rem;
            border-radius: 0.5rem;
            background-color: var(--background-color-primary);
            right: 3rem;
            bottom: -0.5rem;
            transform: rotate(120deg);
            z-index: 1;
          }
        }
      }
    }
  }
}
@media only screen and (max-width: 992px) {
  .quick_content--items.mobile-reverse{
    display: flex;
    flex-direction: column-reverse;
  }
  .quick_content--items.mobile{
    display: flex;
    flex-direction: column;
  }
}
</style>