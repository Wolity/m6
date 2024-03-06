<script setup>
import GameCard from "../components/GameCard.vue";
import * as api from "../api/api.js";
import { onBeforeMount, ref } from "vue";

const games = ref();
onBeforeMount(async () => {
  games.value = await api.GamesCategory("battle-royale");
});
</script>

<template>
  <section>
    <h1 class="title">Royale</h1>
    <div class="card_block">
      <GameCard :game='item' v-for="(item, index) in games" :key="index" />
    </div>
  </section>
</template>

<style>
.title {
  font-size: 40px;
  text-align: center;
  margin: 20px 0;
  color: rgb(255, 255, 255);
}
.card_block {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-gap: 50px;
  margin: 0 50px;
}
</style>
