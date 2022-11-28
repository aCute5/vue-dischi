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
  </div>
</template>

<script>
export default {
  name: "HeaderPage",
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
