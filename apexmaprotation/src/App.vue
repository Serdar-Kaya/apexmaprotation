<script setup>
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://v3.vuejs.org/api/sfc-script-setup.html#sfc-script-setup
import axios from "axios";

const getData = axios
  .get(
    "https://api.mozambiquehe.re/maprotation?version=2&auth=1VzhbvWZZXKKWP5q9mux"
  )
  .then((response) => {
    console.log(response.data.battle_royale.current.map);
  });
</script>

<template>
  <p>bruh</p>
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
