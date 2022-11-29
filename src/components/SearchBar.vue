<template>
  <select
    @change="$emit('pushvalue', valueGenre)"
    v-model="valueGenre"
    class="form-select"
    aria-label="Default select example"
  >
    <option selected>Open this select menu</option>
    <option value="Pop">Pop</option>
    <option value="Jazz">Jazz</option>
    <option value="Metal">Metal</option>
    <option value="Rock">Rock</option>
  </select>
</template>
<script>
export default {
  name: "SearchBar",
  data() {
    return {
      valueGenre: "",
    };
  },
};
</script>

<style></style>
