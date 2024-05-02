<script setup>
import { onMounted, ref } from 'vue';
import { loadState, saveState } from '../utils/Store.js';

const theme = ref(loadState('theme') || 'light')

onMounted(() => {
  document.documentElement.setAttribute('data-bs-theme', theme.value)
})

function toggleTheme() {
  theme.value = theme.value == 'light' ? 'dark' : 'light'
  document.documentElement.setAttribute('data-bs-theme', theme.value)
  saveState('theme', theme.value)
}

</script>

<template>
  <nav class="navbar navbar-dark blueBg pe-3 py-0">
    <router-link class="navbar-brand d-flex" :to="{ name: 'Home' }">
      <div class="d-flex flex-column align-items-center">
        <img alt="logo" src="https://idahocustomironworks.com/wp-content/themes/Idaho/images/Logo.png" height="65"
          title="Home" />
      </div>
    </router-link>
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarText"
      aria-controls="navbarText" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarText">
      <div class="d-flex justify-content-end">
        <div class="blueBg rounded-bottom text-center">
          <ul class="navbar-nav">
            <li>
              <router-link :to="{ name: 'UltraLox' }" class="btn text-light lighten-30 selectable text-uppercase">
                UltraLox
              </router-link>
            </li>
            <li>
              <router-link :to="{ name: 'Commercial' }" class="btn text-light lighten-30 selectable text-uppercase">
                Commercial
              </router-link>
            </li>
            <li>
              <router-link :to="{ name: 'Residential' }" class="btn text-light lighten-30 selectable text-uppercase">
                Residential
              </router-link>
            </li>
            <li>
              <router-link :to="{ name: 'Custom' }" class="btn text-light lighten-30 selectable text-uppercase">
                Custom
              </router-link>
            </li>
          </ul>
          <div>
            <button class="btn text-light" @click="toggleTheme"
              :title="`Enable ${theme == 'light' ? 'dark' : 'light'} theme.`">
              <i class="mdi" :class="theme == 'light' ? 'mdi-weather-sunny' : 'mdi-weather-night'"></i>
            </button>
          </div>
          <!-- LOGIN COMPONENT HERE -->
          <!-- <Login /> -->
        </div>
      </div>
    </div>
  </nav>
</template>

<style scoped>
/* --fds-blue-60: #1877F2;
    --fds-blue-70: #2851A3;
    --fds-blue-80: #1D3C78; */

.blueBg {
  background-color: #2851A3;
}

a:hover {
  text-decoration: none;
}

.nav-link {
  text-transform: uppercase;
}

.navbar-nav .router-link-exact-active {
  border-bottom: 2px solid var(--bs-success);
  border-bottom-left-radius: 0;
  border-bottom-right-radius: 0;
}

nav {
  height: 80px;
}

/* @media screen and (min-width: 576px) {
  nav {
    height: 64px;
  }
} */
</style>
