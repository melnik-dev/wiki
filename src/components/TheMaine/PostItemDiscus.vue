<template>
  <div class="post">
    <h3 class="subtitle">Из новых материалов</h3>
    <h2 class="title">Знаете ли вы?</h2>
    <div class="post__content">
    <ul>
      <li v-for="(item,i) in postDiscusData.listItem" :key="i">{{ item }}</li>
      <button v-if="postDiscusData.btnItem">{{ postDiscusData.btnItem }}</button>
    </ul>
<div class="img__wrapper">
  <img src="../../img/cola.jpg" alt="img">
  <img src="../../img/florencel.jpg" alt="img">
  <img src="../../img/bremer.jpg" alt="img">
</div>
    </div>

  </div>
</template>

<script>

export default {
  name: "PostItemDiscus",
  data() {
    return {
      postDiscusData: {
        listItem:
            [
              "Кокаин в «Кока-коле» (на илл.) заменили на корицу, лимон и кориандр.",
              "Писатель продвигал тайваньскую литературу, но сам писал на языке колонизаторов.",
              "Отказ Финляндии запретить игру про ядерную войну с СССР сильно поднял ей продажи.",
              "Преподаватель японского языка погиб за любовь к России.",
              "Банкир и меценатка (на илл.) помогли 200 деятелям искусства.",
              "Король-солнце, по-видимому, никогда не говорил, что государство — это он.",
              "Американская журналистка организовала перевод книги Вознесенского новым для Запада методом.",
              "НАСА попросило Россию разработать сценарий ликвидации МКС.",
              "В американском мультфильме героиня «Рамаяны» поёт голосом джазовой певицы 1930-х.",
              "Социальная копилка (на илл.) может кукарекать, лаять, мяукать и кричать как осёл.",
              "Флорида получила своё имя из-за того, что испанцы высадились на её берега в пасхальную неделю.",
              "«Партия мёртвых» протестовала против пенсионной реформы с плакатом «Жизнь трудна, но, к счастью, коротка»."
            ],
        btnItem: "Обсудить",
        imgItem: ["cola.jpg", "florencel.jpg", "bremer.jpg"]
      }
    }
  },
  methods: {
    getPic(pic) {
      return require('../../img/' + pic);
    }
  }
}
</script>

<style scoped>
.post {
  border: 1px solid #c8ccd1;
  border-radius: 3px;
  padding: 24px;
}

.subtitle {
  font-size: 14px;
  color: #72777d;
}

button {
  margin-top: 20px;
  padding: 5px 12px;
  font-weight: bold;
}

span {
  font-weight: bold;
}
.post__content{
  display: flex;
}
img{
  margin-top: 30px;
  margin-bottom: 30px;
}
</style>