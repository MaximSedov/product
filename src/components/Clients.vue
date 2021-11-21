<template>
  <section class='clients'>
    <div class='header'>
      <h2>Что говорят клиенты</h2>
    </div>
    <el-row justify='center' class='clients_content'>
      <el-col :xs='22' :sm='22' :md='20' :lg='20' :xl='20'>
        <el-row justify='space-between'>
          <el-col :xs='24' :sm='24' :md='7' :lg='7' :xl='7' class='clients_content-card'>
            <div class='rate'>
              <Icon size='24'>
                <StarEmphasis20Filled />
              </Icon>
              <Icon size='24'>
                <StarEmphasis20Filled />
              </Icon>
              <Icon size='24'>
                <StarEmphasis20Filled />
              </Icon>
              <Icon size='24'>
                <StarEmphasis20Filled />
              </Icon>
              <Icon size='24'>
                <StarEmphasis20Filled />
              </Icon>
            </div>
            <div
              class='text'
            >Lorem ipsum dolor sit amet consectetur adipisicing elit. Atque q corporis odio eaque. Lorem ipsum dolor sit amet.</div>
            <div class='user'>
              <div class='avatar'>
                <el-avatar fit='contain' :size='70' :src='avatar_5'></el-avatar>
              </div>
              <div class='contacts'>
                <div class='username'>Ivan Ivanov</div>
                <div class='userstatus'>Разработчик</div>
              </div>
            </div>
          </el-col>
          <el-col :xs='24' :sm='24' :md='7' :lg='7' :xl='7' class='clients_content-card'>
            <div class='rate'>
              <Icon size='24'>
                <StarEmphasis20Filled />
              </Icon>
              <Icon size='24'>
                <StarEmphasis20Filled />
              </Icon>
              <Icon size='24'>
                <StarEmphasis20Filled />
              </Icon>
              <Icon size='24'>
                <StarEmphasis20Filled />
              </Icon>
              <Icon size='24'>
                <StarEmphasis20Regular />
              </Icon>
            </div>
            <div
              class='text'
            >Lorem ipsum dolor sit amet consectetur adipisicing elit. Atque q corporis odio eaque. Lorem ipsum dolor sit amet.</div>
            <div class='user'>
              <div class='avatar'>
                <el-avatar fit='contain' :size='70' :src='avatar_6'></el-avatar>
              </div>
              <div class='contacts'>
                <div class='username'>Anna Nikolaeva</div>
                <div class='userstatus'>Дизайнер</div>
              </div>
            </div>
          </el-col>
          <el-col :xs='24' :sm='24' :md='7' :lg='7' :xl='7' class='clients_content-card'>
            <div class='rate'>
              <Icon size='24'>
                <StarEmphasis20Filled />
              </Icon>
              <Icon size='24'>
                <StarEmphasis20Filled />
              </Icon>
              <Icon size='24'>
                <StarEmphasis20Filled />
              </Icon>
              <Icon size='24'>
                <StarEmphasis20Filled />
              </Icon>
              <Icon size='24'>
                <StarEmphasis20Regular />
              </Icon>
            </div>
            <div
              class='text'
            >Lorem ipsum dolor sit amet consectetur adipisicing elit. Atque q corporis odio eaque. Lorem ipsum dolor sit amet.</div>
            <div class='user'>
              <div class='avatar'>
                <el-avatar fit='contain' :size='70' :src='avatar_7'></el-avatar>
              </div>
              <div class='contacts'>
                <div class='username'>Vladimir Ivanov</div>
                <div class='userstatus'>Инженер</div>
              </div>
            </div>
          </el-col>

        </el-row>
      </el-col>
    </el-row>
  </section>
</template>

<script>
import StarEmphasis20Filled from '@vicons/fluent/StarEmphasis20Filled'
import StarEmphasis20Regular from '@vicons/fluent/StarEmphasis20Regular'
import { Icon } from '@vicons/utils'
const avatar_5 = require('../assets/avatar-5.webp')
const avatar_6 = require('../assets/avatar-6.webp')
const avatar_7 = require('../assets/avatar-7.webp')
export default {
  data() {
    return {
      avatar_5,
      avatar_6,
      avatar_7,
    }
  },
  components: {
    Icon,
    StarEmphasis20Regular,
    StarEmphasis20Filled,
  },
}
</script>

<style lang="scss">
@import '../colors.scss';
.clients {
  text-align: center;
  .header {
    padding-top: 6rem;
    h2 {
      font-size: 2rem;
      color: var(--text-primary-color) !important;
      margin-bottom: 2rem;
    }
  }
  &_content {
    &-card {
        text-align: left;
      color: var(--text-primary-color);
      border: 2px solid $mainGray;
      border-radius: 1rem;
      padding: 1rem;
      .rate{
          margin-bottom: 1rem;
          .xicon{
              color: $mainYellow;
          }
      }
      .text{
          line-height: 2rem;
          margin-bottom: 1rem;
      }
      .user{
          display: flex;
          align-items: center;
          .avatar{
              margin-right: 1rem;
          }
          .contacts{
              .username{
                  color: $mainGreen;
                  font-weight: bold;
                  font-size: 1.2rem;
              }
              .userstatus{
                  font-weight: bold;
              }
          }
      }
    }
  }
}
@media only screen and (max-width: 992px) {
  .clients_content-card{
    margin-bottom: 2rem;
  }
}
</style>