<template>
  <header>
    <router-link to="/">Main</router-link>
    <router-link to="/fantasy">Fantasy</router-link>
    <router-link to="/royale">Royale</router-link>
    <router-link to="/rgp">Rpg</router-link>
    <router-link to="/shooter">Shooter</router-link>
    <router-link to="/strategy">Strategy</router-link>
  </header>
</template>

<style scoped>
header {
  display: flex;
  justify-content: space-evenly;
  padding: 20px;
  background: bisque ;
  color: #0E38B1;
  font-size: 30px;
}
.router-link-active{
    color:gold;
}
</style>
