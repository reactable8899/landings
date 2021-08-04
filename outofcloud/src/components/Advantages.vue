<template>
  <div class="ourAdvantages">
      <div class="advantagesHeaderText">
        <h2>Преимущества даркстора</h2>
      </div>
      <div class="advantages">
        <div class="advantage" v-for="item in advantages"  :key="item.id">
          <img :src="require('../assets/' + item.img)"/>
          <h4>{{item.headerText}}</h4>
          <p>{{item.text}}</p>
        </div>
      </div>
  </div>
</template>

<script>
export default {
  name: 'Advantages',
  data() {
    return {
      advantages: [
        {
          img: 'ad1.png',
          headerText: 'Нет контакта с посторонними людьми',
          text: 'Заказ формируется из товаров, до которых никто не дотрагивался, как это возможно на полках обычного магазина. Фрукты и овощи отбираются сборщиком вручную.',
          id: 1,
        },
        {
          img: 'ad2.png',
          headerText: 'Заморозка 1 раз',
          text: 'Продукты замораживаются однократно и поддерживаются в этом состоянии, пока не будут доставлены к вам.',
          id: 2,
        },
        {
          img: 'ad3.png',
          headerText: 'Профессиональные морозильные камеры',
          text: 'Товар хранится в промышленных холодильных и морозильных зонах с оптимальными температурными режимами для разных товаров: овощей, фруктов, масла и т. д.',
          id: 3,
        },
        {
          img: 'ad4.png',
          headerText: 'Разделка мяса и рыбы под заказ',
          text: 'Мясо и рыба разделываются непосредственно для вас, а при транспортировке хранятся в специальных боксах с низкой температурой.',
          id: 4,
        },
        {
          img: 'ad5.png',
          headerText: 'Своя пекарня',
          text: 'Знак «Печём сами» на карточках товаров означает, что мы привезём вам свежеиспечённый тёплый хлеб.',
          id: 5,
        },
        {
          img: 'ad6.png',
          headerText: 'Работаем с 1995 года',
          text: 'Мы занимаемся продуктами с 1995 года — все процессы хранения и доставки отточены до мелочей.',
          id: 6,
        },
      ]
    }
  }

}
</script>

<style scoped>
.advantagesHeaderText h2 {
  padding: 40px 0;
  font-size: 36px;
  text-align: center;
}
.ourAdvantages {
  max-width: 1170px;
  margin: 0 auto;
  padding: 0 30px;
}
.advantages {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  grid-gap: 30px;
}
.advantage {
  padding: 40px 30px;
  border-radius: 8px;
  text-align: center;
  background-color: #fff;
}
.advantage:hover {
  background-color: #f1f1f1;
  cursor: pointer;
}
.advantage p {
  font-size: 14px;
  line-height: 25px;
}
@media (max-width: 940px) {
  .advantages {
    display: grid;
    grid-template-columns: 1fr 1fr;
  }
}
@media (max-width: 640px) {
  .advantages {
    display: grid;
    grid-template-columns: 1fr;
  }
  .advantagesHeaderText h2 {
    font-size: 22px;
  }
}

</style>
