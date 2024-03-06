<script setup>
import * as api from "../api/api.js";
import { onBeforeMount, ref } from "vue";
import { useRoute } from "vue-router";
const route = useRoute();
const games = ref();
onBeforeMount(async () => {
  games.value = await api.DetailGame(route.params.id);
});
</script>
<template>
  <div>
    <nav>
      <img
        v-for="(screen, index) in games.screenshots"
        :src="screen.image"
        :key="index"
      />
    </nav>
    <h1>{{ games.title }}</h1>
    <p>{{ games.description}}</p>
  </div>
</template>

<style scoped>
div {
  padding: 20px;
  color: gold;
}
nav {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-evenly;
  grid-gap: 50px;
}
img {
  width: 40%;
}
h1 {
  font-size: 24px;
  text-align: center;
  margin-top: 30px;
}
p {
  font-size: 20px;
  text-align: center;
  margin-top: 30px;
  line-height: 1.2;
}
</style>
