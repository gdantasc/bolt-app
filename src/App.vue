<template>
  <v-app>
    <Header />
    <v-main>
      <Button buttonName="Pesquisar"/>      
    </v-main>
      <Footer />
  </v-app>
</template>

<script>
import Footer from './components/Footer.vue';
import Header from './components/Header.vue';
import Button from './components/Button.vue';


export default {
  name: 'App',

  components: {
    Footer,
    Header,
    Button
  },

  data: () => ({
    //
  }),
};
</script>
