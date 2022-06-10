<template>
  <div class="nav__bar">
    <img src="../../img/logo.png" alt="wiki">
    <NavBarItem v-for="(item, i) in navBarData" :key="i" :links="item.linkItem" :titel="item.titel"/>
    <NavBarItem/>
  </div>
</template>

<script>
import NavBarItem from "./NavBarItem.vue"

export default {
  name: "TheNavBar",
  components: {
    NavBarItem
  },
  data() {
    return {
      navBarData:
          [
            {
              titel: "",
              linkItem: [
                "Заглавная страница",
                "Содержание",
                "Избранные статьи",
                "Избранные статьи",
                "Случайная статья",
                "Текущие события",
                "Пожертвовать"]
            },
            {
              titel: "Участие",
              linkItem: [
                "Сообщить об ошибке",
                "Как править статьи",
                "Сообщество",
                "Форум",
                "Свежие правки",
                "Новые страницы",
                "Справка"]
            },
            {
              titel: "Инструменты",
              linkItem: [
                "Ссылки сюда",
                "Связанные правки",
                "Служебные страницы",
                "Постоянная ссылка",
                "Сведения о странице"]
            },
            {
              titel: "Печать/экспорт",
              linkItem: [
                "Создать книгу",
                "Скачать как PDF",
                "Версия для печати"]
            }
          ]
    }
  }
}
</script>

<style scoped>
nav__bar {
  padding-left: 16px;
}

img {
  width: 160px;
}
</style>
