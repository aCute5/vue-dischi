<template>
  <div class="container-fluid header">
    <a class="navbar-brand" href="#">
      <img
        src="@/img/file-spotify-logo-png-4.png"
        alt="Bootstrap"
        width="50"
        height="50"
      />
    </a>
    <label for="genres">
      <select
        name="genres"
        v-model="GenreStr"
        id="genres"
        @change="$emit('selectedGenre', GenreString)"
      >
        <option value="all">all</option>
        <option value="rock">rock</option>
        <option value="jazz">jazz</option>
        <option value="pop">pop</option>
        <option value="metal">metal</option>
      </select>
    </label>
  </div>
</template>

<script>
export default {
  name: "HeaderPage",
  data() {
    return {
      GenreString: "all",
    };
  },
};
</script>

<style lang="scss" scoped>
.header {
  display: flex;
  align-items: center;
  background-color: #2e3a46;
  height: 10vh;
  justify-content: flex-start;
}
</style>
