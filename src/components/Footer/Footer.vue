<template>
  <v-footer class="footer">
    <div class="footer__icons">
      <v-btn v-for="icon in icons" :key="icon" :icon="icon" class="footer__icon" variant="text" />
    </div>

    <div>{{ dateNow }} — <strong>Thunder Breaker</strong></div>
  </v-footer>
</template>

<script>
export default {
  data() {
    return {
      icons: ['mdi-facebook', 'mdi-twitter', 'mdi-linkedin', 'mdi-instagram']
    };
  },

  computed: {
    dateNow() {
      return new Date().getFullYear();
    }
  }
};
</script>

<style lang="scss" src="./footer.scss" scoped />
