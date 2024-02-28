<script setup>
import GameCard from "../components/GameCard.vue";
</script>

<template>
  <section>
    <h1 class="title">Fantasy</h1>
    <div class="card_block">
      <GameCard />
      <GameCard />
      <GameCard />
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
  margin:0 50px;
}
</style>
