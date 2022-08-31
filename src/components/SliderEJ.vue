<template>
  <div class="container">
    <swiper :slidesPerView="2" :spaceBetween="50" :pagination="{
      type: 'fraction',
    }" :breakpoints="{
  0: {
    slidesPerView: 1,
  },
  400: {
    slidesPerView: 1.5,
  },
  700: {
    slidesPerView: 1.3,
  },
  1200: {
    slidesPerView: 1,
  },
  1800: {
    slidesPerView: 2.5,
  }
}" :navigation="true" :modules="modules" class="mySwiper">
      <swiper-slide v-for="item in data" :key="item.id">
        <div class="slide">
          <div class="slide__bg" v-bind:class="'slide__bg' + item.id">
            <img class="slide__icon" src="../assets/images/i.png" alt="">
            <img class="slide__sale" src="../assets/images/sale.png" alt="">
            <div class="row slide__content">
              <div class="col-5 slide__content__item">
                <h2 class="pt-4">{{  item.title  }}</h2>
                <p>{{  item.text  }}</p>
                <s>{{  item.price  }}</s>
                <h2>{{  item.sale  }}</h2>
              </div>
              <div class="col-6">
                <img :src="require(`../assets/images/${item.image}.png`)" :alt="Ej" class="slide__content__img">
                <div class="slide__content__shadow "></div>
              </div>
            </div>
            <button class="slide__btn">
              <p class="slide__btn_p">+</p>
            </button>
          </div>
        </div>
      </swiper-slide>
    </swiper>
  </div>
</template>

<style lang="scss">
.slide {
  position: relative;
  padding: 70px 0 450px 50px;
  width: 570px;
  height: 400px;

  &__bg1 {
    border-radius: 30px;
    background: #FFEDCD;
    box-shadow: 4px 4px 40px #F1F1F1;
  }

  &__bg2 {
    border-radius: 30px;
    background: #E2F0DF;
    box-shadow: 4px 4px 40px #F1F1F1;
  }

  &__bg3 {
    border-radius: 30px;
    background: #f0e9df;
    box-shadow: 4px 4px 40px #F1F1F1;
  }

  &__bg4 {
    border-radius: 30px;
    background: #f0f0df;
    box-shadow: 4px 4px 40px #F1F1F1;
  }


  &__sale {
    position: relative;
    top: -10px;
    padding-left: 25px;
  }

  &__icon {
    position: relative;
    right: -450px;
    top: 30px
  }

  &__btn {
    width: 100px;
    height: 100px;
    clip-path: polygon(0 100%, 100% 100%, 100% 0);
    position: absolute;
    right: 0px;
    top: 350px;
    border: none;
    background: #fff;
    z-index: 3;

    &:hover {
      background: #1955577e;
    }

    &_p {
      color: #195557;
      font-size: 80px;
      font-weight: 600;
      margin-left: 40px;

      &:hover {
        color: #fff;
      }
    }
  }


  &__content {

    margin: 0px 0px 70px 50px;


    &__item h2 {
      font-weight: 700;
      font-size: 40px;
      line-height: 48px;

      color: #195557;
    }

    &__item p {
      font-family: 'Raleway';
      font-style: normal;
      font-weight: 400;
      font-size: 14px;
      line-height: 22px;

      color: #000000;
    }

    &__img {
      position: relative;
      width: 370px;
      height: 260px;
      left: -85px;
      bottom: -60px;
      transform: rotate(-3deg);
      z-index: 2;
    }

    &__shadow {
      position: relative;
      width: 330px;
      height: 80px;
      left: -65px;
      bottom: 10px;
      background: radial-gradient(50% 50% at 50% 50%, rgba(56, 56, 56, 0.56) 0%, rgba(237, 237, 237, 0) 100%);
      transform: rotate(-5deg);
      overflow: hidden;
      z-index: 1;
    }
  }
}

.swiper {
  z-index: 100;
}

.swiper-button-next:after {
  right: 0;
  color: #195557;
}

.swiper-button-prev:after {
  color: #195557;
  left: 0;
}
</style>

<script>
// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from "swiper/vue";

// Import Swiper styles
import "swiper/css";
import "swiper/css/pagination";
import "swiper/css/navigation";

// import required modules
import { Pagination, Navigation } from "swiper";

export default {
  components: {
    Swiper,
    SwiperSlide,
  },
  setup() {
    return {
      modules: [Pagination, Navigation],
    };
  },
  props: {
    data: {
      type: Array,
      default: () => []
    }
  }
};
</script>

