<script setup>
defineProps({
  game: Object,
});
</script>

<template>
  <div>
    <img :src="game.thumbnail" />
    <h1>{{ game.title }}</h1>
    <p>{{ game.short_descreption }}</p>
    <nav>
      <i class="far fa-clock"></i>
      <h4>{{ game.release_date }}</h4>
    </nav>
    <nav>
      <i class="fas fa-desktop"></i>
      <h4>{{ game.platform }}</h4>
    </nav>
    <router-link :to="{ name: 'detail', params: { id: game.id } }"
      >Подробнее</router-link
    >
  </div>
</template>
<style scoped>
div {
  width: 100%;
  padding: 10px;
  background: #112c7b;
  color: rgb(255, 255, 255);
  border-radius: 10px;
  display: flex;
  flex-direction: column;
}
h1 {
  font-size: 32px;
  margin-top: 20px;
}
p {
  font-size: 20px;
  margin-top: 20px;
}
nav {
  display: flex;
  margin-top: 20px;
}
i,
h4 {
  font-size: 20px;
  margin-right: 10px;
}
a {
  background: rgb(0, 0, 0);
  font-size: 24px;
  padding: 10px 10px;
  margin-top: 20px;
  margin-left: auto;
  border-radius: 10px;
}
</style>
