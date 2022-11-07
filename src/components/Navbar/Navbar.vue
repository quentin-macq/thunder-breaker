<template>
  <v-app-bar class="navbar">
    <v-app-bar-title>Thunder Breaker</v-app-bar-title>

    <nav class="navbar__nav">
      <RouterLink to="/home">Home</RouterLink>
      <RouterLink to="/about">About</RouterLink>
    </nav>

    <v-spacer />
    <v-spacer />
  </v-app-bar>
</template>


<style lang="scss" src="./navbar.scss" scoped />