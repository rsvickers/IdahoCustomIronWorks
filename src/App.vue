<script setup>
import { AppState } from './AppState'
import Navbar from './components/Navbar.vue'


</script>

<template>
  <header>
    <Navbar />
  </header>
  <main>
    <router-view />
  </main>
  <footer class="blueBg text-light">
    Figure this out soon
  </footer>
</template>

<style lang="scss">
@import "./assets/scss/main.scss";

:root {
  --main-height: calc(100vh - 32px - 64px);
}

.blueBg {
  background-color: #2851A3;
}


footer {
  display: grid;
  place-content: center;
  height: 32px;
}
</style>
