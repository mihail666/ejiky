<template>
  <div class="bg1"> </div>
  <div class="bg2"> </div>
  <div class="home ">

    <div class="home__content cotainer-fluid">
      <img class="home_bg" src="../assets/images/Subtract.png" alt="">
      <div class="row">
        <div class="col-md-12 home__content_element">
          <h2>Ёжики</h2>
          <h3>тоже любят молоко</h3>
          <p>Заведите себе ёжика. Он всегда выслушает, не будет мяукать в 5 утра и царапать вашу мебель.</p>
          <button class="ejBtn">Купить ёжика</button>
        </div>
      </div>
    </div>
  </div>
  <div class="contentEj__image">
    <img class="contentEj__image_right" src="../assets/images/image2.png" alt="">
    <div class="contentEj__image_right_sd"></div>
    <img class="contentEj__image_left" src="../assets/images/image3.png" alt="">
    <div class="contentEj__image_left_sd sd"></div>
  </div>

  <div class="about">
    <div class="container-fluid text-center">
      <div class="row about_paddingLeft ">
        <div class="col-md-4 col-xl-2 rr column_padding">
          <div class="about__content col-xs-2 col-md-8 col-xl-6">
            <div class="about__images about__images_bg1 mx-auto d-flex">
              <img src="../assets/images/e.svg" alt="">
            </div>
            <h3>разведение ежиков</h3>
            <p>Собственная ферма, уход и содержание</p>
          </div>
        </div>
        <div class="col-xs-6 col-md-4 col-xl-2 rr">
          <div class="about__content col-xs-2 col-md-8 col-xl-6">
            <div class="about__images about__images_bg2 mx-auto d-flex ">
              <img src="../assets/images/z.svg" alt="">
            </div>
            <h3>здоровье</h3>
            <p>Всегда прививаем и вовремя обследуем ваших будущих питомцев</p>
          </div>
        </div>
        <div class=" col-md-4 col-xl-2 col-xs-6 rr">
          <div class="about__content col-xs-6 col-md-8 col-xl-6">
            <div class="about__images about__images_bg3 mx-auto d-flex ">
              <img src="../assets/images/s.png" alt="">
            </div>
            <h3>любовь и забота</h3>
            <p>Каждому ежику мы дарим много внимания</p>
          </div>
        </div>
      </div>
    </div>
    <SliderEJ :data="SliderContent" />
    <FormEJ />
    <div class="container">
      <div class="col d-md-flex d-block me-auto stockej stockej_padding">
        <img class="p-3" src="../assets/images/e.svg" alt="">
        <h3>У на осталось еще: <a>25 ёжиков</a></h3>
      </div>
      <div class="col d-flex stockej stockej_p">
        Торопитесь! Акция <br> действует до 26. 02. 2023
      </div>
    </div>

  </div>

</template>


<script>
import { SliderContent } from '../data/SliderContent'
import SliderEJ from '@/components/SliderEJ.vue'
import FormEJ from '@/components/FormEJ'
export default {
  name: 'MyHome',
  components: {
    SliderEJ,
    FormEJ
  },
  data() {
    return {
      SliderContent: SliderContent
    }
  }
}
</script>


<style lang="scss">
.home {
  position: relative;
  display: inline-block;
  text-transform: uppercase;
  font-weight: 400;


  &__content img {
    width: 100%;
    height: auto;
  }

  &__content_element {
    /*background: rgba(0,0,0,0.7); (полупрозрачность)*/
    left: 0;
    top: 200px;
    position: absolute;
    width: 100%;
    text-align: center;
  }

  &__content_element h2 {
    font-family: 'Cormorant Infant';
    font-style: normal;
    font-size: 120px;
    font-weight: 900;
    color: #2c614d;
  }

  &__content_element h3 {
    font-family: 'Cormorant Infant';
    font-style: normal;
    font-size: 50px;
    line-height: 60px;

    color: #70908B;
  }

  &__content_element p {
    font-weight: 600;
    font-size: 16px;
    line-height: 16px;
    color: #70908B;
  }


}

.contentEj {
  &__image_right {
    position: absolute;
    width: 510px;
    height: 412px;
    left: -80px;
    top: 710px;
    transform: rotate(-5deg);
    z-index: 3;

    &_sd {
      left: -150px;
      top: 1000px;
      position: absolute;
      width: 480px;
      height: 115px;
      background: radial-gradient(50% 50% at 50% 50%, #9e9b9b 0%, rgba(237, 237, 237, 0) 100%);
      transform: rotate(-10deg);
      z-index: 2;

    }

  }

  &__image_left {
    position: absolute;
    width: 480px;
    height: 331px;
    right: -80px;
    top: 810px;
    z-index: 3;

    &_sd {
      right: -150px;
      position: absolute;
      width: 480px;
      height: 115px;
      top: 1000px;
      background: radial-gradient(50% 50% at 50% 50%, #9e9b9b 0%, rgba(237, 237, 237, 0) 100%);
      transform: rotate(0.5deg);
      z-index: 2;
    }
  }
}

.rr {
  display: flex;
  justify-content: center;
  align-items: center;
}

.about {
  position: relative;
  top: -260px;
  z-index: 4;

  &_paddingLeft {

    display: flex;
    justify-content: center;
    align-items: center;
  }

  &__images {

    width: 150px;
    height: 150px;
    border-radius: 50%;
    display: flex;
    justify-content: center;
    align-items: center;
    margin-bottom: 20px;

    &_bg1 {
      background: #FFEDCD;
      /* iso */
      box-shadow: 4px 4px 20px #C2CCCA, -8px -8px 20px #FFFFFF;
      margin-top: 30px;
    }

    &_bg2 {
      background: #E2F0DF;
      /* iso */
      box-shadow: 4px 4px 20px #C2CCCA, -8px -8px 20px #FFFFFF;
    }

    &_bg3 {
      background: #82b675;
      /* iso */
      box-shadow: 4px 4px 20px #C2CCCA, -8px -8px 20px #FFFFFF;
      margin-top: 30px;

    }
  }
}

.stockej {
  padding: 10px;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
  color: #195557;
  font-size: 18px;
  font-weight: 500;

  &_padding {
    padding-top: 100px;
  }

  & a {
    border-bottom: 2px solid #195557;
  }

  & h3 {
    font-family: 'Cormorant Infant';
    font-style: normal;
    font-weight: 700;
    font-size: 24px;
    line-height: 29px;
  }
}

@media(max-width: 1300px) {
  .home {
    &__content_element {
      top: 140px;
      padding-left: 0px;
      display: block;
      text-align: center;
      align-items: center;
    }

    &__content_element h2 {
      font-size: 100px;
    }

    &__content_element h3 {
      font-size: 40px;
      line-height: 30px;
    }

    &__content_element p {
      margin: 20px 200px;
      font-size: 16px;
      line-height: 20px;
    }
  }

  .contentEj {
    &__image_right {
      width: 310px;
      height: 212px;
      top: 330px;

      &_sd {
        left: -150px;
        top: 450px;
        width: 310px;
        height: 115px;
      }

    }

    &__image_left {
      width: 280px;
      height: 231px;
      right: -30px;
      top: 330px;

      &_sd {
        width: 380px;
        height: 115px;
        top: 450px;
      }
    }
  }

  .about {
    top: -160px;
    z-index: 4;

    &__content {
      padding: 0 0px;
    }

    &__images {
      width: 80px;
      height: 80px;
    }

    &__images_bg1 {
      margin-top: 30px;
    }

    &__images_bg3 {
      margin-top: 30px;
    }
  }

  .FormeEJ {
    &__title {
      font-size: 35px;

    }

    &__bg {
      width: 100%;
      height: 640px;
    }
  }

  .stockej {
    padding: 10px;

    &_padding {
      padding-top: 50px;
    }

    & a {
      border-bottom: 2px solid #195557;
    }

    &_p {
      margin-bottom: 50px;
    }
  }

}

@media(max-width:1200px) {
  .about {
    top: 0px;

    &__images_bg1 {
      margin-top: 0px;
    }

    &__images_bg3 {
      margin-top: 0px;
    }
  }
}

@media(max-width:920px) {

  .contentEj__image_right {
    display: none;

    &_sd {
      display: none;
    }
  }

  .contentEj__image_left {
    top: 260px;

    &_sd {
      top: 380px;
    }
  }

  .about {
    top: 40px;
  }

  .home {
    &__content_element {
      top: 150px;
      padding-left: 0px;
      display: block;
      text-align: center;
      align-items: left;
    }

    &__content_element h2 {
      font-size: 70px;
    }

    &__content_element h3 {
      font-size: 30px;
      line-height: 30px;
    }

    &__content_element p {
      font-size: 16px;
      line-height: 20px;
      margin: 30px 100px 0 100px;
    }
  }

  .stockej {
    padding: 10px;

    &_padding {
      padding-top: 50px;
    }

    & a {
      border-bottom: 2px solid #195557;
    }

    &_p {
      margin-bottom: 50px;
    }
  }
}

@media(max-width:400px) {
  .home {
    padding: 0 0px;

    &__content_element {
      top: 50px;
      padding: 40px;
      display: block;
      text-align: left;
      align-items: left;
    }

    &__content_element h2 {
      font-size: 40px;
    }

    &__content_element h3 {
      font-size: 24px;
      line-height: 15px;
    }

    &__content_element p {
      margin: 10px 0px;
      font-size: 16px;
      text-transform: none;
    }

    &__content img {
      width: 100%;
      height: 450px;
    }
  }

  .about {
    top: -90px;

    &__images {
      width: 100px;
      height: 100px;
    }

    &__images_bg1 {
      margin-top: 0px;
    }

    &__images_bg3 {
      margin-top: 0px;
    }
  }

  .contentEj {
    &__image_left {
      top: 310px;

      &_sd {
        top: 420px;
      }
    }
  }

  .rr {
    display: block;
    width: 50%;
  }

  .column_padding {
    margin-right: 200px;
  }

  .FormeEJ {
    &__bg {
      width: 100%;
      min-height: 140vh;
    }

    &__title {
      padding: 30px 20px 10px 20px;

      font-size: 35px;
    }

    }
    .controlF {
      font-size: 16px;
      padding: 20px;
      &__coments{
        padding: 10px 10px 130px 10px;
      }
    }

    .btn {
      border-radius: 60px;
      padding: 15px 40px;
      margin-top: 10px;
      font-weight: 700;
      font-size: 16px;
    }

    .form-check {
      padding: 20px 0 0 50px;
      font-weight: 700;
      font-size: 16px;
    }

    .btnBuy {
      box-shadow: 4px 4px 20px #C2CCCA, -8px -8px 20px #FFFFFF;
      padding: 20px 80px;
      color: #fff;
    }

    .stockej {
      padding-top: 20px;
      display: flex;
      justify-content: center;
      align-items: center;
      text-align: center;
      color: #195557;
      font-size: 20px;
      font-weight: 500;

      &_padding {
        padding-top: 40px;
      }

      & a {
        border-bottom: 2px solid #195557;
      }

      & h3 {
        font-family: 'Cormorant Infant';
        font-style: normal;
        font-weight: 700;
        font-size: 24px;
        line-height: 29px;
      }
    }
  }
</style>
