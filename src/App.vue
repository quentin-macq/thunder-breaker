<template>
  <v-app>
    <v-main class="app">
      <Header/>
      <Home />
    </v-main>
  </v-app>
</template>

<script>
import Header from "./components/Header/Header.vue";
import Home from "./pages/Home/Home.vue";

export default {
  components: {Home, Header}
}
</script>

<style lang="scss" scoped src="./app.scss"/>