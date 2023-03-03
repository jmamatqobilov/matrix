<template>
  <v-container>
    <v-row justify="center">
      <v-col sm="12" align-self="center" md="6" lg="4">
        <v-card width="368" height="320">
          <v-progress-circular model-value="40" color="deep-orange-lighten-2">{{ value }}</v-progress-circular>
        </v-card>
      </v-col>
      <v-col sm="12"  align-self="center" md="6" lg="4">
        <v-card width="368" height="320">
          <v-progress-circular model-value="40" color="deep-orange-lighten-2">{{ value }}</v-progress-circular>
        </v-card>
      </v-col>
      <v-col sm="12"  align-self="center" md="6" lg="4">
        <v-card width="368" height="320">
          <v-progress-circular model-value="40" color="deep-orange-lighten-2">{{ value }}</v-progress-circular>
        </v-card>
      </v-col>
  </v-row>
  <div class="">
    <div class="">
      All
    </div>
  </div>
  </v-container>


</template>

<script>
import SimpleCard from "."
export default {
  name: 'HomeView',

  components: {

  },

  data() {
    return {
      tab: 1,
      value: 0
    }
  },
};
</script>

<style scoped>
.card {
  border-radius: 20px;
  box-shadow: 3px 8px 20px 8px rgba(117, 173, 188, 0.1)
}
</style>
