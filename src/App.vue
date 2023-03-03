<template>
  <v-app>
    <div class="index-view">
      <Index />
    </div>
  </v-app>
</template>

<script>
import Index from './views/index';
export default {
  name: 'App',
  components: {
    Index
  },
  data: () => ({

  }),
}
</script>

<style scoped>
* {
  box-sizing: border-box;
}



.navbar {
  border-bottom-left-radius: 42px;
  background: linear-gradient(261.11deg, #77CABA 0%, #229A87 90.84%);
}

.navbar-container {
  display: flex;
}

.index-view {
  padding-top: 40px;
}
</style>
