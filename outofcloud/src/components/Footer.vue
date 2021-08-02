<template>
  <div class="footer">
    <div class="footerContent">
      <img src="../assets/logo.png" alt="" class="logo">
      <div class="contacts">
        <div class="numbers">
          <div class="">
            <p>Москва</p>
            <h1>+7 495 797-57-77</h1>
          </div>
          <div class="">
            <p>Санкт-Петербург</p>
            <h1>+7 812 385-99-55</h1>
          </div>
        </div>
        <div class="socials">
          <div>
            <img src="../assets/f.svg" alt="">
          </div>
          <div>
            <img src="../assets/vk.svg" alt="">
          </div>
          <div>
            <img src="../assets/in.svg" alt="">
          </div>
          <div>
            <img src="../assets/ok.svg" alt="">
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Footer',

}
</script>

<style scoped>
  h1, h2, p {
    margin: 0;
    padding: 0;
  }
  .footer {
    height: 270px;
    background: linear-gradient(0deg, #043E44, #043E44), #CBE07D;
    display: flex;
    justify-content: center;
  }
  .footerContent {
    width: 1170px;
    padding: 0 30px;
  }
  .footerContent > img {
    margin-top: 50px;
  }
  .numbers {
    width: 100%;
    display: flex;
    justify-content: space-between;
  }
  .socials {
    width: 100%;
    display: flex;
    justify-content: flex-end;
    align-items: center;
  }
  .socials div {
    margin-left: 40px;
  }
  .numbers h1 {
    font-size: 26px;
    margin-top: 5px;
  }
  .contacts {
    margin-top: 40px;
    display: flex;
    justify-content: space-between;
    color: #fff;
  }
  @media (max-width: 1050px) {
    .numbers {
      display: block;
    }
    .numbers > div {
      margin-bottom: 20px;
    }
    .footer {
      height: 350px;
    }
  }
  @media (max-width: 640px) {
    .contacts {
      display: block;
    }
    .numbers h1 {
      font-size: 28px;
    }
    .footer {
      height: 400px;
    }
    .socials {
      padding-top: 20px;
      display: flex;
      justify-content: space-between;
    }
    .socials div {
      margin: 0;
    }
    .footerContent {
      padding: 0 60px;
    }
  }
  @media (max-width: 420px) {
    .footer {
      height: 400px;
    }
    .numbers h1 {
      font-size: 22px;
    }
  }
</style>
