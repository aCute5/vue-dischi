<template>
  <div id="app">
    <header-page @pushvalue=""></header-page>
    <MainPage />
  </div>
</template>

<script>
import HeaderPage from "@/components/HeaderPage.vue";
import MainPage from "./components/MainPage.vue";

export default {
  name: "App",
  components: {
    MainPage,
    HeaderPage,
  },
  props: {
    filter: String,
  },
};
</script>

<style lang="scss">
@import "~bootstrap/scss/bootstrap";
@import url("https://fonts.googleapis.com/css2?family=Lato&display=swap");

body {
  font-family: "Lato", sans-serif;
}
</style>
