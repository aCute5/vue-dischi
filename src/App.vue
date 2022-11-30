<template>
  <div id="app">
    <header-page @selectedGenre="newGenre"></header-page>
    <MainPage :stringValue="searchString" />
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
  data() {
    return {
      searchString: "all",
    };
  },
  methods: {
    newGenre(valore) {
      this.searchString = valore;
    },
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
