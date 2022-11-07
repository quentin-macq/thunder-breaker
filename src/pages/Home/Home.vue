<template>
  <v-container>
    <v-col>
      <div>
        <v-card color="#f4f4f4">
          <div @click="dialog = true">
            <v-img src="https://cdn.vuetifyjs.com/images/cards/sunshine.jpg" cover height="180" />

            <v-card-title class="pt-3">
              test
              <span>(test)</span>
            </v-card-title>

            <v-card-text>
           test
            </v-card-text>
          </div>
        </v-card>

        <v-dialog v-model="dialog">
          <v-card color="#f4f4f4">
            <div>
              <v-icon
                  color="white"
                  icon="mdi-close"
                  right
                  size="30"
                  @click="dialog = false"
              />
            </div>

            <v-card-text>
              test
            </v-card-text>

            <v-card-actions>
              <v-btn
                  color="#e52c4d"
                  target="_blank"
                  variant="outlined"
                  @click="dialog = false"
              >
                <span>test</span>
              </v-btn>
            </v-card-actions>
          </v-card>
        </v-dialog>
      </div>
    </v-col>
  </v-container>
</template>

<script>
export default {
  data() {
    return {
      dialog: false
    }
  }
}
</script>

<style scoped>

</style>