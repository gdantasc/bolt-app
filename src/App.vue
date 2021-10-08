<template>
  <v-app>
    <Header />
    <v-main>
      <Button buttonName="Pesquisar"/>      
      <Modal />

    </v-main>
      <Footer />
  </v-app>
</template>

<script>
import Footer from './components/Footer.vue';
import Header from './components/Header.vue';
import Button from './components/Button.vue';
import Modal from './components/Modal.vue';


export default {
  name: 'App',

  components: {
    Footer,
    Header,
    Button,
    Modal
  },

  data: () => ({
    //
  }),
};
</script>
