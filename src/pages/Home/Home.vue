<template>
  <v-container class="home">
    <div v-for="(item, index) in content" :key="index" class="home__container">
      <div class="home__text">
        <h1> {{ item.title }} </h1>
        <div> {{ item.text }} </div>

        <v-btn class="home__text__button" rounded width="120"> voir + </v-btn>
      </div>

      <div class="home__img-wrapper">
        <img :src="'/public/assets/img/' + item.img" alt="circuit breaker">
      </div>
    </div>
  </v-container>
</template>

<script>
import {content} from "../../data/content";

export default {
  data() {
    return {
      content: content
    }
  }
}
</script>

<style lang="scss" scoped src="./home.scss"/>