<template>
  <div class="col-2">
    <div class="card" style="width: 9rem">
      <img :src="disc.poster" />
      <div class="card-body">
        <h5 class="card-title">{{ disc.title }}</h5>
        <p class="card-text">
          {{ disc.author }}
        </p>
        <p class="card-text">
          {{ disc.year }}
        </p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "CardDisc",
  props: {
    disc: Object,
  },
};
</script>

<style lang="scss" scoped>
.card {
  height: 20rem;
  text-align: center;
  background-color: #2e3a46;
}
.card h5 {
  color: white;
}
.card-text {
  color: #585d62;
}
.card img {
  padding: 1rem;
}
</style>
