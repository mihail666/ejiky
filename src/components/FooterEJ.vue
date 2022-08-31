<template>
  <div class="container-fluid footer">
    <div class="row footer__bg">
      <div class="footer__bg1">
        <ul class="footer__nav d-flex ">
          <li class="footer__title col-3">
            <img class="footer__logo" src="../assets/images/Logo.svg" alt="">
            <div class="col-xl-12 col-12">
              <p class="footer__logo_p">
                Все права защищены. <br>
                Указанная стоимость товаров и условия их приобретения действительны на текущую дату.</p>
            </div>
          </li>
          <li class="nav-item col-xl-1 offset-xl-2 col-md-2  dropdown">
            <a class="nav-link active p-2" href="#" role="button" data-bs-toggle="dropdown" aria-expanded="false"><span
                class="dropdownTitle">
                <h3>Каталог</h3>
              </span></a>
            <ul class="dropdown-menu">
              <li><a class="dropdown-item" href="#"><span>Ёжики</span></a></li>
              <li><a class="dropdown-item" href="#"><span>Питание</span></a></li>
              <li><a class="dropdown-item" href="#"><span>переноски</span></a></li>
              <li><a class="dropdown-item" href="#"><span>Лекарства</span></a></li>
              <li>
                <hr class="dropdown-divider">
              </li>
              <li><a class="dropdown-item" href="/">Home</a></li>
            </ul>
          </li>
          <li class="nav-item col-xl-1 col-md-2 p-2 d-md-flex d-none" v-for="(menu, index) in headerMenuList" :key="index">
            <router-link class="nav-link active navBtn" aria-current="page" :to="menu.path">
              <span></span><span></span><span></span><span></span>
              <h3>{{ menu.name }}</h3>
            </router-link>
          </li>
          <li class="nav-item mx-2"><a href="https://investor.twitterinc.com/" target="_ blank"><img
                src="../assets/images/1.svg" alt=""></a></li>
          <li class="nav-item mx-2"><a href="https://instagram.com/" target="_ blank"><img src="../assets/images/2.svg"
                alt=""></a></li>
          <li class="nav-item mx-2"><a href="https://www.facebook.com/" target="_ blank"><img
                src="../assets/images/3.svg" alt=""></a></li>
          <li>
            <div class="nav-item col-xl col-md-d-none footer__nav_p p-2">
              <h3>+7 (965) 569-89-98</h3>
            </div>
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
import { menuList } from '../constants/menuList.js'
export default {
  props: {
    msg: String
  },
  data() {
    return {
      headerMenuList: menuList
    }
  }
}
</script>

<style lang="scss">
.footer {
  color: #fff;

  &__bg {
    position: relative;
    background: #70908B;
    height: 250px;
    padding-top: 90px;
  }
  &__bg1{
    background: #70908B;
  }

  &__nav {
    &_p {
      margin-left: 50px;
    }
  }

  &__nav li {
    list-style-type: none;
  }

  &__nav h3 {

    font-family: 'Cormorant Infant';
    font-style: normal;
    font-weight: 700;
    font-size: 16px;
    line-height: 19px;
    text-transform: uppercase;
    color: #FFFFFF;
  }

  &__nav p {
    font-family: 'Raleway';
    font-style: normal;
    font-weight: 400;
    font-size: 9px;
    color: #FFFFFF;
    margin: 20px 0;

  }
}
@media(max-width:400px){
  .footer{
    &__bg {
    padding-top: 40px;
  }
    &__logo{
      
    
    width: 70px;
    height: 40px;
  
    }
  }
}

</style>