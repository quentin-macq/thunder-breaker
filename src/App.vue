<template>
  <v-app>
    <v-main class="app">
      <Header />
      <Home />
      <Footer />
    </v-main>
  </v-app>
</template>

<script>
import Header from './components/Header/Header.vue';
import Home from './pages/Home/Home.vue';
import Footer from './components/Footer/Footer.vue';

export default {
  components: { Footer, Home, Header }
};
</script>

<style lang="scss" scoped src="./app.scss" />
