<template>
  <nav class="navbar navbar-expand-lg">
    <div class="container-fluid">
      <button class="navbar-toggler  " type="button" data-bs-toggle="offcanvas" data-bs-target="#navbarOffcanvasLg"
        aria-controls="navbarOffcanvasLg">
        <span class="navbar-toggler-icon col-md-2"></span>
      </button>
      <a class="col-xxl col-xl-6" href="/"><img class="navbar__logo" src="../assets/images/Logo.svg" alt="ej" /></a>
      <div class="collapse navbar-collapse offcanvas offcanvas-end" tabindex="-1" id="navbarOffcanvasLg"
        aria-labelledby="navbarOffcanvasLgLabel">
        <div class="offcanvas__header d-xl-none">
          <button type="button" class="btn-close text-reset d-xl-none" data-bs-dismiss="offcanvas" aria-label="Закрыть"></button>
          <a href="/"><img class="offcanvas__logo d-xl-none" src="../assets/images/Logo.svg" alt="ej" /></a>
        </div>
        <ul class="navbar-nav">
          <li class="nav-item dropdown col-xxl-1 offset-xxl-6 col-xl-4">
            <a class="nav-link dropdown-toggle active " href="#" role="button" data-bs-toggle="dropdown"
              aria-expanded="false"><span class="dropdownTitle">Каталог</span></a>
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
          <li class="nav-item col-xxl-1 col-xl-4" v-for="(menu, index) in headerMenuList" :key="index">
            <router-link class="nav-link active navBtn" aria-current="page" :to="menu.path">
              <span></span><span></span><span></span><span></span>
              {{  menu.name  }}
            </router-link>
          </li>
          <li class="nav-item col-xxl-2 col-xl-6  mr-auto d-flex ">
            <div class="images images_bg1 d-xl-flex d-md-none">
              <img src="../assets/images/Vector.svg" alt="">
            </div>
            <div class="nav-item navbar__item-n col-xl-8">+7 (965) 569-89-98</div>
          </li>

          <li class="nav-item col-xxl-1 col-xl-4 d-xl-block d-md-none">
            <a class="" href="#">
              <img class="" src="../assets/images/Vector.png" alt="" /></a>
          </li>
        </ul>
      </div>
    </div>
  </nav>

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
.navbar {
  position: absolute;
  background-color: none;
  padding-top: 70px;
  padding-left: 40px;
  height: 60px;
  z-index: 5;

  &__logo {
    left: 60px;
    z-index: 5;
  }

  &__item-n {
    font-size: 16px;
    font-weight: 700;
  }
}

.navbar-nav .nav-link.active {
  font-family: 'Cormorant Infant';
  font-style: normal;
  font-weight: 700;
  font-size: 16px;
  line-height: 19px;
  text-transform: uppercase;
  color: #195557;
}

.images {
  position: relative;
  top: -10px;
  margin-right: 10px;
  width: 50px;
  height: 50px;
  border-radius: 50%;
  display: inline-flex;
  justify-content: center;
  align-items: center;

  &_bg1 {
    background: linear-gradient(1.36deg, #B0D3CE 12.29%, #FFEDCE 83.89%);
    box-shadow: -4px -4px 20px #FFFFFF, 4px 4px 20px #CFD7D3;
    border-radius: 40px;
  }
}



.dropdownTitle {
  border-bottom: none;
  transition: .1s;

  &:hover {
    display: inline;
    border-bottom: 2px solid #195557
  }
}

.dropdown-toggle::after {
  content: "";
  text-decoration: solid #195557;
  margin-left: -6em;

}

.dropdown-menu {
  background: #FFFEFE;
  box-shadow: 4px 4px 20px #C2CCCA;
  border-radius: 8px;
  --bs-dropdown-link-hover-bg: none;
  --bs-dropdown-link-active-bg: #19555781;
}

.dropdown-item {
  font-family: 'Cormorant Infant';
  font-style: normal;
  margin: 10px 0;

  font-weight: 700;
  font-size: 16px;
  line-height: 19px;
  text-transform: uppercase;

  color: #195557;

  &:hover {
    display: inline;
    border-bottom: 2px solid #195557
  }
}

.offcanvas {
  &__logo {
    margin: 0 0 0 40px;
    left: 0;
  }
  &__header{
    position: relative;
    left: -80px;
    display: flex;
    justify-content:space-between;
    align-items: center;
    
    padding-top: 40px;
    
  }
}

.offcanvas li {
  padding-top: 30px;
  margin-right: 100px;
}

.offcanvas.offcanvas-end {
  left: 0;
}

@media(max-width:1300px) {
  .navbar {
    padding: 20px;

    &__logo {

      display: block;
      margin-left: 320px;
      text-align: center;
      background-position: center;
    }
  }

  .navbar__item-n {
    padding-top: 10px;
  }
}
@media(max-width: 400px){
  .navbar {
 

  &__logo {
    margin-left: 0;
    margin: 0 120%;
    width: 70px;
    height: 40px;
  }
}
.navbar-toggler-icon{
  width: 20px;
  height: 20px;
}
}
</style>
