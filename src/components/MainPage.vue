<template>
  <div class="container-fluid">
    <div v-if="arrDiscs" class="row">
      <CardDisc
        v-for="Objdisc in arrDiscs"
        :key="Objdisc.poster"
        :disc="Objdisc"
      ></CardDisc>
    </div>
    <div v-else class="loading">
      <i class="fa-solid fa-spinner"></i>
    </div>
  </div>
</template>

<script>
import axios from "axios";
import CardDisc from "@/components/CardDisc.vue";
export default {
  name: "MainPage",
  components: {
    CardDisc,
  },
  data() {
    return {
      arrDiscs: null,
      urlApi: "https://flynn.boolean.careers/exercises/api/array/music",
    };
  },
  created() {
    axios.get(this.urlApi).then((axiosResponse) => {
      console.log(axiosResponse);
      this.arrDiscs = axiosResponse.data.response;
    });
  },
};
</script>

<style lang="scss" scoped>
.container-fluid {
  background-color: #1e2d3b;
  height: 80vh;
  width: 100vw;
  display: flex;
  justify-content: center;
  align-items: center;
}
.row {
  width: 800px;
  gap: 2rem;
}
.loading {
  font-size: 120px;
  color: white;
  animation: lds-dual-ring 1.2s linear infinite;
}
@keyframes lds-dual-ring {
  0% {
    transform: rotate(0deg);
  }
  100% {
    transform: rotate(360deg);
  }
}
</style>
