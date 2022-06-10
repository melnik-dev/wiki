<template>
  <div class="page__wrapper">
    <TheNavBar/>
    <TheMaine/>
  </div>

</template>

<script>
import TheNavBar from "./components/TheNavBar/TheNavBar.vue";
import TheMaine from "./components/TheMaine/TheMaine.vue";
import indexDB from "./indexDB";

export default {
  components: {
    TheNavBar,
    TheMaine
  }
}

</script>

<style>
body {
  background-color: #f6f6f6;
}
img {
  max-width: 100%;
  display: block;
}
a {
  text-decoration: none;
  cursor: pointer;
  color: #0645ad;
}
a:hover {
  text-decoration: underline;
}
.page__wrapper {
  display: grid;
  grid-template-columns: 14% 86%;
}
</style>
