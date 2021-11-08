<script setup>
import axios from "axios";

const getMapName = axios
  .get(
    "https://api.mozambiquehe.re/maprotation?version=2&auth=1VzhbvWZZXKKWP5q9mux"
  )
  .then((response) => {
    document.getElementById("firstp").innerHTML =
      response.data.battle_royale.current.map;
  });

const getMapImage = axios
  .get(
    "https://api.mozambiquehe.re/maprotation?version=2&auth=1VzhbvWZZXKKWP5q9mux"
  )
  .then((response) => {
    document.getElementById("firstimg").innerHTML =
      response.data.battle_royale.current.asset;
  });

const getMapTime = axios
  .get(
    "https://api.mozambiquehe.re/maprotation?version=2&auth=1VzhbvWZZXKKWP5q9mux"
  )
  .then((response) => {
    console.log(response.data.battle_royale.current.remainingTimer);
  });
</script>

<template>
  <div id="main">
    <div>
      <h1>BATTLE ROYALE PUBS</h1>
      <img src="" alt="" id="firstimg" />
      <div class="image"></div>
      <p id="firstp"></p>
    </div>
    <div>
      <h1>BATTLE ROYALE RANKED</h1>
      <div class="image">there goes image</div>
      <p>this should be remaning time</p>
    </div>
    <div>
      <h1>ARENAS PUBS</h1>
      <div class="image">there goes image</div>
      <p>this should be remaning time</p>
    </div>
    <div>
      <h1>ARENAS RANKED</h1>
      <div class="image">there goes image</div>
      <p>this should be remaning time</p>
    </div>
  </div>
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}

#main {
  display: flex;
  align-items: center;
  margin: 0;
  border: black;
  text-align: center;
  flex-direction: column;
}

.image {
  display: flex;
  height: 42rem;
  width: 69rem;
  justify-content: center;
  align-items: center;
}
</style>
