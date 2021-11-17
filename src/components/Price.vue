<template>
  <section class='price'>
    <div class='header'><h2>Цены</h2></div>
    <el-row justify='center' class='price_content'>
      <el-col :xs='22' :sm='22' :md='20' :lg='20' :xl='20'>
        <el-row justify='space-between'>
          <el-col :xs='24' :sm='24' :md='7' :lg='7' :xl='7' class='price_content-card'>
            <div class='title'>Бесплатно</div>
            <div class='subtitle'>Lorem, ipsum dolor.</div>
            <div class='cost'>
              <div class='cost-number'>0</div>
              <div class='cost-currency'>
                <div class='icon'>
                  <Icon size='24'>
                    <CurrencyRubel viewBox="5 0 24 24"/>
                  </Icon>
                </div>
                <div class='period'>За сутки</div>
              </div>
            </div>
            <div class='features'>
              <div class='text'>Lorem, ipsum.</div>
              <div class='text'>Lorem, ipsum dolor.</div>
              <div class='text'>Lorem, ipsum.</div>
            </div>
            <div class='button'>
              <el-button style='font-weight:bold;margin-bottom: 2rem; margin-top: 1rem' type='success'>Купить сейчас</el-button>
            </div>
          </el-col>
          <el-col :xs='24' :sm='24' :md='7' :lg='7' :xl='7' class='price_content-card'>
            <div class='title'>Стандарт</div>
            <div class='subtitle'>Lorem, ipsum dolor.</div>
            <div class='cost'>
              <div class='cost-number'>10</div>
              <div class='cost-currency'>
                <div class='icon'>
                  <Icon size='24'>
                    <CurrencyRubel viewBox="5 0 24 24"/>
                  </Icon>
                </div>
                <div class='period'>За сутки</div>
              </div>
            </div>
            <div class='features'>
              <div class='text'>Lorem, ipsum.</div>
              <div class='text'>Lorem, ipsum dolor.</div>
              <div class='text'>Lorem, ipsum.</div>
            </div>
            <div class='button'>
              <el-button style='font-weight:bold;margin-bottom: 2rem; margin-top: 1rem' type='success'>Купить сейчас</el-button>
            </div>
          </el-col>
          <el-col :xs='24' :sm='24' :md='7' :lg='7' :xl='7' class='price_content-card'>
            <div class='title'>Премиум</div>
            <div class='subtitle'>Lorem, ipsum dolor.</div>
            <div class='cost'>
              <div class='cost-number'>20</div>
              <div class='cost-currency'>
                <div class='icon'>
                  <Icon size='24'>
                    <CurrencyRubel viewBox="5 0 24 24"/>
                  </Icon>
                </div>
                <div class='period'>За сутки</div>
              </div>
            </div>
            <div class='features'>
              <div class='text'>Lorem, ipsum.</div>
              <div class='text'>Lorem, ipsum dolor.</div>
              <div class='text'>Lorem, ipsum.</div>
            </div>
            <div class='button'>
              <el-button style='font-weight:bold; margin-bottom: 2rem; margin-top: 1rem' type='success'>Купить сейчас</el-button>
            </div>
          </el-col>
        </el-row>
      </el-col>
    </el-row>
  </section>
</template>

<script>
import CurrencyRubel from '@vicons/tabler/CurrencyRubel'
import { Icon } from '@vicons/utils'
export default {
  data() {
    return {}
  },
  components: {
    Icon,
    CurrencyRubel,
  },
}
</script>

<style lang="scss">
@import '../colors.scss';
.price {
  text-align: center;
  background-color: $mainGray;
  padding-bottom: 2rem;
  .header {
    padding-top: 6rem;
    h2{
      font-size: 2rem;
    color: $mainBlack !important;
    margin-bottom: 2rem;
    }
    
  }
  &_content {
    &-card {
      background-color: $white;
      color: $mainBlack;
      -webkit-box-shadow: 0px 5px 10px 2px rgba(34, 60, 80, 0.2);
      -moz-box-shadow: 0px 5px 10px 2px rgba(34, 60, 80, 0.2);
      box-shadow: 0px 5px 10px 2px rgba(34, 60, 80, 0.2);
      border-radius: 1rem;
      .title {
        margin-top: 2rem;
        font-size: 2rem;
        font-weight: bold;
        margin-bottom: 2rem;
      }
      .subtitle {
        margin-bottom: 2rem;
      }
      .cost {
        display: flex;
        justify-content: center;
        align-items: center;
        margin-bottom: 2rem;
        &-number {
          font-size: 4rem;
          color: $mainGreen;
          font-weight: bold;
          margin-right: 1rem;
        }
        &-currency {
          text-align: left;
          .icon {
            margin-bottom: 0;
            .xicon {
              color: $mainGreen;
            }
          }
          .period {
            color: $darkGray;
          }
        }
      }
      .features {
        .text {
          margin-bottom: 1rem;
          font-weight: bold;
        }
      }
      &:hover{
        cursor:pointer;
        color: $white;
        background-color: $mainGreen;
        .cost{
          &-number{
            color: $white;
          }
          &-currency{
            .icon{
              .xicon{
                color: $white;
              }
            }
            .period{
              color: $white;
            }
          }
        }
        .el-button{
          background-color: $white;
          color: $mainGreen;
        }
      }
    }
  }
}
@media only screen and (max-width: 992px) {
  .price_content-card{
    margin-bottom: 2rem;
  }
}
</style>