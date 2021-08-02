<template>
  <div class="SliderBlock">
    <div class="SliderText">
      <h1>Взгляните на процесс сборки</h1>
      <h1>своими глазами</h1>
    </div>
    <div class="slider">
      <div class="arrowLeft">
        <img src="../assets/arrow1.png" alt="" @click="prevList">
      </div>
      <div class="sliderList">
        <div class="list">
          <img :src="require('../assets/' + currentListImg)"/>
          <h4>{{currentListHeaderText}}</h4>
          <p>{{currentListText}}</p>
        </div>
      </div>
      <div class="arrowRight">
        <img src="../assets/arrow2.png" alt="" @click="nextList">
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Slider',
  data() {
    return {
      listCount: 0,
      currentListImg: 'image1.png',
      currentListHeaderText: 'Привезём точно по списку',
      currentListText: 'Сборщик берëт с собой наручный терминал, на котором он видит весь список покупок для каждого заказа.',
      slider: [
        {
          id: 1,
          img: 'image1.png',
          headerText: 'Привезём точно по списку',
          text: 'Сборщик берëт с собой наручный терминал, на котором он видит весь список покупок для каждого заказа.'
        },
        {
          id: 2,
          img: 'image2.png',
          headerText: 'Довезëм в сохранности даже яйца',
          text: 'Бережно транспортируем контейнеры, фиксируя их стяжными ремнями. Системы охлаждения поддерживают температурный режим.'
        },
        {
          id: 3,
          img: 'image3.png',
          headerText: 'Шампунь не положат рядом с рыбой',
          text: 'Собираем и упаковываем ваш заказ с заботой: соблюдаем принципы товарного соседства и учитываем вес товара.'
        },
        {
          id: 4,
          img: 'image4.png',
          headerText: 'За свежесть и качество отвечаем',
          text: 'Выделены специальные зоны, в том числе холодная и морозильная.'
        },
        {
          id: 5,
          img: 'image5.png',
          headerText: 'Собираем быстро и эффективно',
          text: 'Для улучшения эргономики пространства товары размещены от тяжëлых к лëгким, находящимся уже в конечной зоне упаковки.'
        },
      ]
    }
  },
  methods: {
    nextList() {
      this.listCount++
      if (this.listCount <= this.slider.length - 1) {
        this.currentListImg = this.slider[this.listCount].img
        this.currentListHeaderText = this.slider[this.listCount].headerText
        this.currentListText = this.slider[this.listCount].text
      } else {
        this.listCount = 0
        this.currentListImg = this.slider[this.listCount].img
        this.currentListHeaderText = this.slider[this.listCount].headerText
        this.currentListText = this.slider[this.listCount].text
      }
    },
    prevList() {
      this.listCount--
      if (this.listCount >= 0) {
        this.currentListImg = this.slider[this.listCount].img
        this.currentListHeaderText = this.slider[this.listCount].headerText
        this.currentListText = this.slider[this.listCount].text
      } else {
        this.listCount = this.slider.length - 1
        this.currentListImg = this.slider[this.listCount].img
        this.currentListHeaderText = this.slider[this.listCount].headerText
        this.currentListText = this.slider[this.listCount].text
      }
    }
  }

}
</script>

<style scoped>
.SliderBlock {
  padding-bottom: 100px;
  max-width: 1170px;
  margin: 0 auto;
}
.SliderText {
  padding-top: 100px;
  padding-bottom: 50px;
}
.SliderText h1 {
  margin: 0;
  text-align: center;
}
.slider {
  padding: 0 30px;
  display: flex;
  justify-content: space-around;
}
.arrowLeft {
  display: flex;
  align-items: center;
  cursor: pointer;
}
.arrowRight {
  display: flex;
  align-items: center;
  cursor: pointer;
}
.sliderList {
  width: 640px;
  padding: 50px;
  background-color: #fff;
  height: 450px;
  box-shadow: 0px 0px 15px 5px rgba(34, 60, 80, 0.2);
}
.list {
  text-align: center;
}
.list img {
  width: 600px;
}
.list p {
  font-size: 14px;
  line-height: 25px;
}
@media (max-width: 1200px) {
  .sliderList {
    width: 540px;
    height: 370px;
  }
  .list img {
    width: 500px;
  }
}
@media (max-width: 950px) {
  .sliderList {
    width: 420px;
    height: 330px;
  }
  .list img {
    width: 420px;
  }
}
@media (max-width: 750px) {
  .sliderList {
    width: 360px;
    height: 310px;
  }
  .list img {
    width: 370px;
  }
  .SliderText {
    font-size: 12px;
  }
}
@media (max-width: 650px) {
  .sliderList {
    width: 300px;
    height: 310px;
  }
  .list img {
    width: 300px;
  }
}
</style>
