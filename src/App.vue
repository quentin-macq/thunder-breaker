<template>
  <v-app>
    <v-layout>
      <Navbar />
      <v-main class="app">
        <v-container>
          &#128540;
          <RouterView/>
        </v-container>
      </v-main>
    </v-layout>
  </v-app>
</template>

<script>
import {RouterLink, RouterView} from 'vue-router';
import Home from "./pages/Home/Home.vue";
import Navbar from "./components/Navbar/Navbar.vue";

export default {
  components: {Navbar, Home, RouterLink, RouterView}
}
</script>

<style lang="scss" scoped src="./app.scss"/>