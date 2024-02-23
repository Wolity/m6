<script setup>
import Header from "./components/Header.vue";

import Main from "./views/Main.vue";
</script>

<template>
  <div class="app">
    <Header />
    <Main />
  </div>
</template>

<style scoped>
.app {
  background: #005397;
  min-height: 100vh;
}
</style>
