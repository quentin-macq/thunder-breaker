<template>
  <v-container class="home">
    <div v-for="(item, index) in content" :key="index" class="home__container">
      <div class="home__text">
        <h2 class="home__text__subtitle">{{ item.title }}</h2>
        <div class="home__text__content">
          <span v-if="!item.showMore">{{ shortDescription(item.description) }}</span>
          <span v-else>{{ item.description }}</span>
        </div>

        <v-btn
          v-if="!item.showMore"
          class="home__text__button"
          rounded
          width="120"
          @click="showMore(item)"
        >
          voir +
        </v-btn>
      </div>

      <div class="home__img-wrapper">
        <img :src="'/assets/img/' + item.img" alt="circuit breaker" />
      </div>
    </div>
  </v-container>
</template>

<script>
import { content } from '@/data/content';

export default {
  data() {
    return {
      content,
      maxLength: 240
    };
  },

  methods: {
    shortDescription(description) {
      description = description.substr(0, this.maxLength);
      return description.substr(0, description.lastIndexOf(' ')) + '...';
    },

    showMore(item) {
      item.showMore = true;
    }
  }
};
</script>

<style lang="scss" scoped src="./home.scss" />
