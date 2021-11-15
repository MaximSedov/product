<template>
  <section class='customer'>
    <el-row  justify='center' class='customer_content'>
      <el-col :xs='8' :sm='6' :md='10' :lg='13' :xl='13'>
        <div class='customer_content--img'>
          <el-image :src='customer' fit='cover'></el-image>
        </div>
      </el-col>
      <el-col :xs='8' :sm='6' :md='10' :lg='7' :xl='7'>
        <div class='subtitle'>
          <span>Lorem, ipsum dolor.</span>
        </div>
        <div class='title'>Cлужба поддержки клиентов</div>
        <div
          class='text'
        >Lorem ipsum, dolor sit amet consectetur adipisicing elit. Ab culpa iure quaerat odit. Quo molestias odit tempora repellendus voluptas, omnis aperiam libero vero porro in doloribus</div>
        <div class='list'>
          <div class='list-item'>
            <div class='icon'>
              <Icon size='24'>
                <Checkmark16Filled />
              </Icon>
            </div>
            <div>Lorem ipsum dolor, sit amet consectetur adipisicing.</div>
          </div>
          <div class='list-item'>
            <div class='icon'>
              <Icon size='24'>
                <Checkmark16Filled />
              </Icon>
            </div>
            <div>Lorem ipsum dolor, sit amet consectetur adipisicing.</div>
          </div>
          <div class='list-item'>
            <div class='icon'>
              <Icon size='24'>
                <Checkmark16Filled />
              </Icon>
            </div>
            <div>Lorem ipsum dolor, sit amet consectetur adipisicing.</div>
          </div>
        </div>
      </el-col>
    </el-row>
  </section>
</template>

<script>
const customer = require('../assets/customer.png')
import { Checkmark16Filled } from '@vicons/fluent'
import { Icon } from '@vicons/utils'
export default {
  data() {
    return {
      customer,
    }
  },
  components: {
    Icon,
    Checkmark16Filled,
  },
}
</script>

<style lang="scss">
@import '../colors.scss';
.customer {
  margin-top: 6rem;
  &_content {
    display: flex;
    justify-content: space-between;
    align-items: center;
    .subtitle {
      font-weight: bold;
      font-size: 1.1rem;
      margin-bottom: 1rem;
    }
    .title {
      font-size: 2rem;
      font-weight: bold;
      margin-bottom: 2rem;
    }
    .text {
      margin-bottom: 2rem;
    }
    &--img {
      display: flex;
      justify-content: start;
    }
    .list {
      &-item {
        display: flex;
        align-items: center;
        margin-bottom: 2rem;
        .xicon {
          padding: 0.3rem;
          border-radius: 0.9rem;
          margin-right: 2rem;
          color: $white;
        }
        &:nth-child(1) .xicon{
            background-color: $mainYellow;
        }
        &:nth-child(2) .xicon{
            background-color: $mainRed;
        }
        &:nth-child(3) .xicon{
            background-color: $mainBlue;
        }
      }
    }
  }
}
</style>