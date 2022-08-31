<template>
  <div class="FormEJ ">
    <div class="container">
      <div class="FormeEJ__bg">
        <h2 class="FormeEJ__title">
          Заполните заявку и мы забронируем для Вас нового друга
        </h2>
        <div class="row btn-group  " role="group" aria-label="Basic outlined example">
            <div class="col-xl-2 col-md-4">
              <button type="button" class="btn btn-outline-success">хочу ёжика для себя</button>
            </div>
            <div class="col-xl-2 col-md-4">
              <button type="button" class="btn btn-outline-success">хочу ёжика для детей</button>
            </div>
            <div class="col-xl-2 col-md-4">
              <button type="button" class="btn btn-outline-success">хочу ёжика для разведения</button>
            </div>
          <div class="col-xl-3 col-md-6 ">
            <div class="form-check">
              <input class="form-check-input" type="radio" name="gridRadios" id="gridRadios1" value="option1" checked>
              <label class="form-check-label" for="gridRadios1">
                хочу ёжика для разведения
              </label>
            </div>
            <div class="form-check">
              <input class="form-check-input" type="radio" name="gridRadios" id="gridRadios2" value="option2">
              <label class="form-check-label" for="gridRadios2">
                Мне нужны 3-4 ёжика
              </label>
            </div>
          </div>

          <div class="col-xl-3 col-md-6">
            <div class="form-check">
              <input class="form-check-input" type="radio" name="gridRadios" id="gridRadios3" value="option3" checked>
              <label class="form-check-label" for="gridRadios3">
                Мне нужны 3 и более ёжиков
              </label>
            </div>
            <div class="form-check">
              <input class="form-check-input" type="radio" name="gridRadios" id="gridRadios4" value="option4">
              <label class="form-check-label" for="gridRadios4">
                Пока присматриваюсь
              </label>
            </div>
          </div>

        </div>

        <div class="row mx-1">
          <div class="col-md-4">
            <label for="formGroupExampleInput" class="form-label"></label>
            <input type="text" class="control controlF" id="formGroupExampleInput" placeholder="Ваше имя">
          </div>
          <div class="col-md-4">
            <label for="formGroupExampleInput" class="form-label"></label>
            <input type="text" class="control controlF" id="formGroupExampleInput" placeholder="Ваш телефон">
          </div>
          <div class="col-md-4">
            <label for="formGroupExampleInput" class="form-label"></label>
            <input type="text" class="control controlF" id="formGroupExampleInput" placeholder="Ваш E-mail">
          </div>
          <div class="col-md-12">
            <label for="formGroupExampleInput" class="form-label"></label>
            <input type="text" class="control controlF controlF__coments" id="formGroupExampleInput"
              placeholder="Ваш комментарий">
          </div>
        </div>
        <div class="col-xl-12 offset-xl-5 col-md-5 offset-md-4 pt-5 col-10 offset-2 ">
          <button class="btnBuy" type="button">Купить ёжика</button>
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss">
.FormeEJ {
  position: relative;

  &__bg {
    width: 100%;
    height: 57vh;
    margin-top: 50px;
    background: #EAEEEF;
    border-radius: 30px;
  }

  &__title {
    font-family: 'Cormorant Infant';
    font-style: normal;
    padding: 50px 30px 20px 30px;
    font-weight: 700;
    font-size: 45px;
    line-height: 54px;

    color: #195557;

  }
}

.btn {
  background: #ffffff;
  border: 2px solid #70908B;
  border-radius: 61px;
  padding: 20px 40px;
  margin-left: 20px;
  font-family: 'Cormorant Infant';
  font-style: normal;
  font-weight: 700;
  font-size: 20px;
  line-height: 17px;
  /* identical to box height */
  color: #195557;

  &:hover {
    background: #70908B;
    color: #fff;
  }
}

.form-check {
  font-family: 'Cormorant Infant';
  font-style: normal;
  padding: 10px 0 0 20px;
  font-weight: 700;
  font-size: 20px;
  line-height: 20px;
  /* identical to box height */
  color: #70908B;
}

.form-check-input:checked {
  background-color: #70908B;
  ;
  border-color: #70908B;
}

.controlF {
  background: #ffffff;
  border-radius: 8px;
  padding: 30px;
  font-family: 'Raleway';
  font-style: normal;
  font-weight: 400;
  font-size: 20px;
  line-height: 16px;
  border: none;
  color: #195557;
  display: block;
  width: 100%;
  transition: border-color .15s ease-in-out, box-shadow .15s ease-in-out;


  &__coments {
    background: #F8F8F8;
    border-radius: 8px;
    padding: 10px 10px 100px 10px;
    font-family: 'Raleway';
    font-style: normal;
    font-weight: 400;
    font-size: 14px;
    line-height: 16px;
  }
}

.btnBuy {
  background: #70908B;
  /* iso */

  box-shadow: 4px 4px 20px #C2CCCA, -8px -8px 20px #FFFFFF;
  border-radius: 40px;
  border: none;
  padding: 20px 80px;
  font-family: 'Raleway';
  font-style: normal;
  font-weight: 700;
  font-size: 14px;
  line-height: 16px;

  color: #fff;

  &:hover {
    background: linear-gradient(90.14deg, #B0D3CE -2.41%, #FFEDCE 99.79%);
    /* iso */

    box-shadow: 4px 4px 20px #C2CCCA, -8px -8px 20px #FFFFFF;
    border-radius: 40px;

    color: #195557;
  }

}
</style>