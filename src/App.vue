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
  <footer class="blueBg text-light py-4">
    <div class="d-flex fs-3">
      <a href="https://www.facebook.com/ICEFabrication/" title="ICIW Facebook" target="_blank">
        <i class="mdi mdi-facebook mx-3"></i>
      </a>
      <a href="https://www.instagram.com/idahocustomironworks/" title="ICIW Instagram" target="_blank">
        <i class="mdi mdi-instagram"></i>
      </a>
    </div>
  </footer>
</template>

<style lang="scss">
@import "./assets/scss/main.scss";

:root {
  --main-height: calc(100vh - 32px - 64px);
}

.blueBg {
  background-color: #2851A3;
  // background-color: #FBC926;
}


footer {
  display: grid;
  place-content: center;
  height: 32px;
}
</style>
