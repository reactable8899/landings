<template>
  <div class="purchase">
    <div class="container">
      <div class="discountsBlock">
        <div class="discounts">
          <div class="discountsImg">
            <img src="../assets/disc1.svg" alt="">
          </div>
          <div class="discountsText">
            <h1>Скидка</h1>
            <h2>1500 P</h2>
            <p><b>–500 ₽</b> на первые три заказа</p>
            <p>по промокоду NEW</p>
          </div>
        </div>
        <div class="plus">
          <img src="../assets/plus.png" alt="">
        </div>
        <div class="discounts">
          <div class="discountsImg">
            <img src="../assets/disc2.svg" alt="">
          </div>
          <div class="discountsText">
            <h1>Бесплатная</h1>
            <h2>Доставка</h2>
            <p>первого заказа</p>
          </div>
        </div>
      </div>
    </div>
    <div class="purchaseBtnBlock">
      <span class="purchaseBtn" @click="showPopUpBtn">К покупкам</span>
    </div>
    <div class="popup-bg" v-show="showPopUp">
      <div class="popup">
        <h1 v-show="!popupContent">Спасибо :)</h1>
        <div class="closePopUp">
          <span @click="closePopUpBtn" v-show="!popupContent">Закрыть</span>
        </div>
        <div class="popupContent" v-show="popupContent">
          <p>Заполните поле</p>
          <div class="popupInput">
              <input type="text" name="" placeholder="Введите Email" v-model="email">
          </div>
          <div class="form">
            <div class="closePopUp">
              <span  @click="closePopUpBtn">Закрыть</span>
            </div>
            <div class="sendBtn">
              <button @click="sendBtn">Отправить</button>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Header',
  data() {
    return {
      showPopUp: false,
      popupContent: true,
      email: ''
    }
  },
  methods: {
    showPopUpBtn() {
      this.showPopUp = true
    },
    closePopUpBtn() {
      this.showPopUp = false
    },
    sendBtn() {
      if (this.email != '') {
        setTimeout(() => {
          const response = this.email
          console.log(response)
          this.popupContent = false
        }, 1000);
        console.log(this.email)
      } else {
        alert('Заполните поле !')
      }
    }

  }

}
</script>

<style scoped>
.popup h1 {
  text-align: center;
  color: #9dc776;
  padding: 30px;
}
.form {
  margin-top: 30px;
  display: flex;
  justify-content: space-between;
}
.sendBtn {
  display: flex;
  justify-content: flex-end;
}
.sendBtn button {
  border: none;
  font-size: 16px;
  padding: 10px 16px;
  border-radius: 6px;
  cursor: pointer;
  background-color: rgb(197, 126, 126);
  color: #fff;
}
.popupInput {
  padding: 30px;
  width: 100%;
}
.popupInput input {
  padding: 14px;
  width: 80%;
  border: none;
  border-bottom: 1px solid #000;
  font-size: 16px;
}
.closePopUp span:hover {
  background-color: #9dc776;
  color: #fff;
  cursor: pointer;
  border-radius: 5px;
}
.closePopUp span {
  padding: 10px 22px;
}
.closePopUp {
  display: flex;
  justify-content: flex-end;
}
.popup-bg {
  position: fixed;
  width: 100%;
  height: 100%;
  top: 0;
  left: 0;
  background: rgba(0,0,0,0.8);
}
.popup {
  position: absolute;
  top: 50%;
  left: 50%;
  width: 600px;
  background-color: #fff;
  padding: 20px;
  transform: translate(-50%, -50%);
}
.purchase {
  background-color: #fff;
  height: 600px;
}
.container {
  max-width: 1170px;
  margin: 0 auto;
  padding: 0 30px;
}
.discountsBlock {
  padding-top: 70px;
  display: grid;
  grid-template-columns: 3fr 1fr 3fr;
}
.discounts {
  display: flex;
  justify-content: space-around;
  border: 2px solid #eee;
  padding: 40px;
}
.discountsImg {
  width: 90px;
  height: 90px;
  background-color: #7DB945;
  border-radius: 50%;
  display: flex;
  justify-content: center;
  align-items: center;
}
.discountsImg img {
  width: 50px;
  height: 25px;
}
.plus {
  display: flex;
  justify-content: center;
  align-items: center;
}
.discountsText h1 {
  margin-top: 20px;
  margin-bottom: 0;
  font-size: 38px;
}
.discountsText h2 {
  margin: 0;
  font-size: 34px;
  color: #7DB945;
}
.discountsText p {
  line-height: 15px;
}
.purchaseBtnBlock {
  padding-top: 70px;
  display: flex;
  justify-content: center;
}
.purchaseBtn {
  cursor: pointer;
  padding: 18px 120px;
  background-color: #7DB945;
  font-size: 32px;
  color: #fff;
  border-radius: 15px;
  font-weight: bold;
}
@media (max-width: 1050px) {
  .discounts {
    display: block;
  }
  .plus {
    display: none;
  }
  .discountsBlock {
    display: grid;
    grid-template-columns: 1fr 1fr;
    grid-gap: 30px;
  }
  .discountsImg {
    margin: 0 auto;
  }
  .discountsText {
    text-align: center;
  }
  .purchaseBtnBlock {
    padding-top: 50px;
  }
}
@media (max-width: 640px) {
  .discountsBlock {
    display: grid;
    grid-template-columns: 1fr;
  }
  .purchase {
    height: 1000px;
  }
  .purchaseBtn {
    padding: 18px 80px;
    background-color: #7DB945;
    font-size: 28px;
  }
}
@media (max-width: 400px) {
  .discounts {
    padding: 20px;
  }
  .purchase {
    height: 850px;
  }
  .discountsText h1 {
    margin-bottom: 0;
    font-size: 32px;
  }
  .discountsText h2 {
    margin: 0;
    font-size: 28px;
    color: #7DB945;
  }
  .discountsText p {
    line-height: 15px;
    font-size: 14px;
  }
  .purchaseBtn {
    padding: 18px 60px;
    font-size: 24px;
  }
}
</style>
