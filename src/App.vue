<template>
  <v-app>
    <Header />
    <v-main>
      <Button buttonName="Pesquisar"/>      
      <!-- <Card />   -->    
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
// import Card from './components/Card.vue';


export default {
  name: 'App',

  components: {
    Footer,
    Header,
    Button,
    Modal,
    // Card
  },

  data: () => ({
    //
  }),
};
</script>
