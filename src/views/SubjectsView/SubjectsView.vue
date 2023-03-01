<template>
  <v-card width="368px" height="320px" color="white" class="card">
    <v-col cols="12" sm="3">
      <v-progress-circular model-value="40" color="deep-orange-lighten-2">{{ value }}</v-progress-circular>
    </v-col>
  </v-card>
</template>

<script>


// Components


export default {
  name: 'HomeView',

  components: {

  },

  data() {
    return {
      tab: 1,
      value:0
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
