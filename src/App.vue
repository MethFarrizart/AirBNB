<template>
  <v-app>
    <v-main>
      <Airbnb/>
    </v-main>
  </v-app>
</template>

<script>
import Airbnb from './components/Airbnb.vue';

export default {
  name: 'App',

  components: {
    Airbnb
},

  data: () => ({
    //
  }),
}
</script>
