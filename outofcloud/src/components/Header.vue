<template>
  <div class="header">
    <img src="../assets/fon.png" alt="">
      <div class="container">
        <img src="../assets/logo.png" alt="" class="logo">
        <h1>Что такое даркстор?</h1>
        <p>Это магазин-склад без покупателей.</p>
        <p>Именно здесь, а не в розничном</p>
        <p>магазине собирают ваши заказы.</p>
        <div class="swipe">
          <img src="../assets/swipe.png" alt="" class="swipe">
          <span>Свайп вниз</span>
        </div>
      </div>
  </div>
</template>

<script>
export default {
  name: 'Header',

}
</script>

<style scoped>
* {
  padding: 0;
  margin: 0;
}
body {
  overflow: hidden;
}
.header {
  width: 140%;
  position: relative;
  left: -20%;
  margin-top: -530px;
  padding-top: 530px;
  height: 510px;
  border-radius: 38%;
  overflow: hidden;
}
.header::after {
  content: '';
  display: block;
  position: absolute;
  left: 0;
  right: 0;
  top: 0;
  bottom: 0;
  background: linear-gradient(90deg, #2A3D43 10%,transparent);
}
.header img {
  position: absolute;
  top: 530px;
  left: 0;
  right: 0;
  height: 530px;
  width: 72%;
  margin: 0 auto;
}
.main {
  margin-top: 20px;
}
.container {
  position: relative;
  max-width: 1170px;
  margin: 0 auto;
  z-index: 1;
}
.container img {
  position: relative;
  top: 0;
  width: 150px;
  height: 40px;
  margin: 0;
  margin-top: 75px;
}
.container h1 {
  font-size: 44px;
  color: #fff;
  margin-top: 60px;
  margin-bottom: 20px;
}
.container p {
  font-size: 26px;
  color: #fff;
  margin-top: 15px;
}
.swipe {
  display: flex;
  justify-content: center;
}
.swipe img {
  margin-top: 40px;
  width: 70px;
  height: 50px;
  cursor: pointer;
}
.swipe span {
  font-size: 22px;
  color: #fff;
  margin-top: 50px;
  margin-left: 20px;
  cursor: pointer;
}
@media (max-width: 1300px) {
  .container > img {
    position: relative;
    left: 100px;
  }
  .container p , h1 {
    position: relative;
    left: 100px;
  }
}
@media (max-width: 1050px) {
  .container > img {
    position: relative;
    left: 200px;
  }
  .container p , h1 {
    position: relative;
    left: 200px;
  }
}
@media (max-width: 640px) {
  .container > img {
    position: relative;
    left: 180px;
  }
  .container p , h1 {
    position: relative;
    left: 180px;
  }
  .container p {
    font-size: 20px;
  }
  .container h1 {
    font-size: 36px;
  }
}
@media (max-width: 500px) {
  .container > img {
    position: relative;
    left: 120px;
  }
  .container p , h1 {
    position: relative;
    left: 120px;
  }
  .container p {
    font-size: 18px;
  }
  .container h1 {
    font-size: 32px;
  }
}
@media (max-width: 400px) {
  .container > img {
    position: relative;
    left: 100px;
  }
  .container p , h1 {
    position: relative;
    left: 100px;
  }
  .container p {
    font-size: 14px;
  }
  .container h1 {
    font-size: 24px;
  }
}
</style>
