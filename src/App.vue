<template>
  <v-app>
    <Header />
    <v-main>
    </v-main>
      <Footer />
  </v-app>
</template>

<script>
import Footer from './components/Footer.vue';
import Header from './components/Header.vue';


export default {
  name: 'App',

  components: {
    Footer,
    Header
  },

  data: () => ({
    //
  }),
};
</script>
