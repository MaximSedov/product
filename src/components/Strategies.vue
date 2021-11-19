<template>
  <section class='strategies'>
    <el-row justify='center' class='strategies_content'>
      <el-col :xs='22' :sm='22' :md='20' :lg='20' :xl='20'>
        <el-row justify='start'>
          <el-col :xs='24' :sm='24' :md='24' :lg='24' :xl='24' class='header'>
            <div class='header_title'>Стратегии</div>
            <div class='header_subtitle'>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Distinctio, dignissimos.</div>
          </el-col>
        </el-row>
        <el-row justify='center'>
          <el-col :xs='24' :sm='24' :md='24' :lg='24' :xl='24'>
            <Carousel snap-align='center' :items-to-show='3' :breakpoints='breakpoints' :wrap-around='true'>
              <Slide v-for='(slide, index) in slides' :key='slide.index'>
                <div class='carousel__item'>
                  <div class='item'>
                    <div class='image'>
                      <el-image style='width: 100%; height: 100%' :src='require("@/assets/photo-"+(index+1)+".jpg")' fit='cover' lazy></el-image>
                    </div>
                    <div class='subtitle'>
                      <div class='author'>
                        By
                        <strong>{{slide.author}}</strong>
                      </div>
                      <el-divider direction='vertical'></el-divider>
                      <div class='date'>{{slide.date}}</div>
                    </div>
                    <div class='title'>{{slide.title}}</div>
                  </div>
                </div>
              </Slide>
              <template #addons>
                <Pagination />
              </template>
            </Carousel>
          </el-col>
        </el-row>
      </el-col>
    </el-row>
  </section>
</template>

<script>
import { defineComponent } from 'vue'
import { Carousel, Slide, Pagination } from 'vue3-carousel'
import 'vue3-carousel/dist/carousel.css'

export default defineComponent({
  data() {
    return {
      slides: [
        {
          img: 'strategies_1',
          author: 'Alex Wake',
          date: '10 Ноября 2021',
          title: 'Lorem ipsum dolor sit. Lorem, ipsum dolor.',
        },
        {
          img: 'strategies_2',
          author: 'Ivan Loginov',
          date: '09 Ноября 2021',
          title: 'Lorem ipsum dolor sit. Lorem, ipsum dolor.',
        },
        {
          img: 'strategies_3',
          author: 'Alex Wake',
          date: '08 Ноября 2021',
          title: 'Lorem ipsum dolor sit. Lorem, ipsum dolor.',
        },
        {
          img: 'strategies_1',
          author: 'Alex Wake',
          date: '10 Ноября 2021',
          title: 'Lorem ipsum dolor sit. Lorem, ipsum dolor.',
        },
        {
          img: 'strategies_2',
          author: 'Ivan Loginov',
          date: '09 Ноября 2021',
          title: 'Lorem ipsum dolor sit. Lorem, ipsum dolor.',
        },
        {
          img: 'strategies_3',
          author: 'Alex Wake',
          date: '08 Ноября 2021',
          title: 'Lorem ipsum dolor sit. Lorem, ipsum dolor.',
        }
      ],

      breakpoints: {
        // 700px and up
        0: {
          itemsToShow: 1,
          snapAlign: 'start',
        },
        // 1024 and up
        1024: {
          itemsToShow: 3,
          snapAlign: 'start',
        },
      },
    }
  },
  components: {
    Pagination,
    Carousel,
    Slide,
  },
})
</script>

<style lang="scss">
@import '../colors.scss';
.strategies {
  padding-top: 6rem;
  background-color: $mainGray;
  &_content {
    display: flex;
    justify-content: space-between;
    align-items: center;
    .header {
      text-align: center;
      &_title {
        font-size: 2rem;
        color: $mainBlack !important;
        margin-bottom: 2rem;
        font-weight: bold;
      }
      &_subtitle {
        font-weight: bold;
        color: $mainBlack !important;
        margin-bottom: 2rem;
      }
    }
    .carousel {
      width: 100%;
      &__slide {
      }
      &__track {
      }
      &__item {
        width: 100%;
        display: block;
        min-height: 360px;
        text-align: left;
        .item {
          margin: 1rem;
          border: 1px solid $darkGray;
          border-radius: 1rem;
          &:hover{
            cursor: pointer;
            .title{
              color: $mainGreen;
            }
          }
        }
        .image {
          width: 100%;
          height: 12rem;
          margin-bottom: 1rem;
          .el-image {
            border-top-left-radius: 1rem;
            border-top-right-radius: 1rem;
          }
        }
        .subtitle {
          padding: 1rem;
          display: flex;
          align-items: center;
          .author {
          }
        }
        .title {
          padding: 1rem;
          color: var(--text-secondary-color);
          font-size: 1.5rem;
          line-height: 2rem;
          font-weight: bold;
          margin-bottom: 1rem;
        }
      }
      &__pagination {
        margin-top: 2rem;
        &-button {
          background-color: $lightGreenOpacity;
          width: 1rem;
          height: 1rem;
          border-radius: 50%;
        }
        &-button--active {
          background-color: $darkGreen;
        }
      }
    }
  }
}
@media only screen and (max-width: 768px) {
  
}
</style>