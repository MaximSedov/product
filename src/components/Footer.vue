<template>
  <section class='footer'>
    <el-row justify='center' class='footer_content'>
      <el-col :xs='22' :sm='22' :md='20' :lg='20' :xl='20'>
        <el-row>
          <el-col :xs='12' :sm='12' :md='6' :lg='6' :xl='6'>
            <div class='block'>
              <div class='logo'>
                <el-image style='width: 40px; height: 40px' :src='logo' fit='cover'></el-image>Product
              </div>
              <div class='links'>
                <Icon size='24'>
                  <BrandInstagram />
                </Icon>
                <Icon size='24'>
                  <BrandFacebook />
                </Icon>
                <Icon size='24'>
                  <BrandTwitter />
                </Icon>
              </div>
            </div>
          </el-col>
          <el-col :xs='12' :sm='12' :md='6' :lg='6' :xl='6'>
              <div class="block">
                  <div class="title">Ресуры</div>
                  <div class="nav-link">Продукт</div>
                  <div class="nav-link">Клиенты</div>
                  <div class="nav-link">Цены</div>
                  <div class="nav-link">Контакты</div>
              </div>
          </el-col>
          <el-col :xs='12' :sm='12' :md='6' :lg='6' :xl='6' class="desktop">
              <div class="block">
                  <div class="title">Юридические вопросы</div>
                  <div class="nav-link">Финансирование</div>
                  <div class="nav-link">Политика конфиденциальности</div>
                  <div class="nav-link">Условия обслуживания</div>
              </div>
          </el-col>
          <el-col :xs='12' :sm='12' :md='6' :lg='6' :xl='6' class="desktop">
              <div class="block">
                  <div class="form_title">Lorem ipsum dolor sit amet consectetur.</div>
                  <el-input v-model="input" placeholder="Почта" />
                   <el-button style='font-weight:bold' type='success'>Отправить</el-button>
              </div>
          </el-col>
          <el-col :xs='12' :sm='12' :md='6' :lg='6' :xl='6' class="mobile">
              <div class="block">
                  <div class="form_title">Lorem ipsum dolor sit amet consectetur.</div>
                  <el-input v-model="input" placeholder="Почта" />
                   <el-button style='font-weight:bold' type='success'>Отправить</el-button>
              </div>
          </el-col>
          <el-col :xs='12' :sm='12' :md='6' :lg='6' :xl='6' class="mobile">
              <div class="block">
                  <div class="title">Юридические вопросы</div>
                  <div class="nav-link">Финансирование</div>
                  <div class="nav-link">Политика конфиденциальности</div>
                  <div class="nav-link">Условия обслуживания</div>
              </div>
          </el-col>
        </el-row>
        <el-row justify='center'>
            <el-col :xs='22' :sm='22' :md='24' :lg='24' :xl='24'>
                <div class="footer_content--text">
                    dev by <a href="https://sdvmxm.ru" target="_blank" rel="noopener noreferrer">sdvmxm</a> / design by Figmaland && канал @figma2html
                </div>
            </el-col>
        </el-row>
      </el-col>
    </el-row>
  </section>
</template>

<script>
import BrandInstagram from '@vicons/tabler/BrandInstagram'
import BrandFacebook from '@vicons/tabler/BrandFacebook'
import BrandTwitter from '@vicons/tabler/BrandTwitter'
import { Icon } from '@vicons/utils'
const logo = require('../assets/cubes.png')
export default {
  data() {
    return {
      logo,
    }
  },
  components: {
    Icon,
    BrandInstagram,
    BrandFacebook,
    BrandTwitter,
  },
}
</script>

<style lang="scss">
@import '../colors.scss';
.footer {
  padding-top: 6rem;
  &_content {
    .block {
      .logo {
        display: flex;
        align-items: center;
        font-weight: bold;
        font-size: 1.5rem;
        color: $mainBlack;
        .el-image {
          margin-right: 1rem;
        }
      }
      .links {
        display: flex;
        align-items: center;
        margin-top: 1rem;
        .xicon {
          color: $mainGreen;
          padding: 0.5rem;
          border-radius: 50%;
          background-color: $mainGray;
          margin-right: 0.5rem;
          &:last-child{
              margin-right: 0;
          }
          &:hover{
              cursor: pointer;
              color: $darkGreen;
          }
        }
      }
      .title{
          color: $mainBlack;
          font-size: 1.3rem;
          margin-bottom: 1.5rem;
          font-weight: bold;
      }
      .nav-link{
          color: $mainBlack;
          margin-bottom: 1rem;
          &:hover{
              cursor: pointer;
              color: $mainGreen;
          }
      }
      .form_title{
          color: $mainBlack;
          font-size: 1.3rem;
          margin-bottom: 1.5rem;
          font-weight: bold;
      }
      .el-input{
          margin-bottom: 1.5rem;
      }
    }
    &--text{
        text-align: center;
        margin-top: 2rem;
        margin-bottom: 2rem;
        a{
            text-decoration: none;
            color: $mainGreen;
            &:hover{
                color: $darkGreen;
                cursor: pointer;
                text-decoration: underline;
            }
        }
    }
  }
}
@media only screen and (max-width: 992px) {
  .footer_content .desktop{
      display: none;
  }
  .footer_content .block .el-input{
    padding-right: 1rem !important;
    box-sizing: border-box;
  }
}
@media only screen and (min-width: 992px) {
  .footer_content .mobile{
      display: none;
  }
}
</style>