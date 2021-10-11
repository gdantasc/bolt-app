<template>
  <v-app>
    <Header />
    <v-main>
      <Button buttonName="Pesquisar" />

      <Card v-for="event in events" :key="event" :event="event" />
      <!-- <Modal /> -->
    </v-main>
    <Footer />
  </v-app>
</template>

<script>
import Footer from "./components/Footer.vue";
import Header from "./components/Header.vue";
import Button from "./components/Button.vue";
// import Modal from './components/Modal.vue';
import Card from "./components/Card.vue";

export default {
  name: "App",
  data: () => ({
    events: [
      {
        id: "dd847ded-6667-4fed-894b-a9db1f94c60f",
        name: "Noite de louvor",
        day: "12/09/2021",
        start_date_time: "10:30",
        end_date_time: "11:30",
        vacancies: "20",
        available_vacancies: "0",
        description: null,
        location: {
          id: "ef58aea9-315e-46ac-90c6-661242df1844",
          name: "Igreja Católica Santo André",
          street: "Padre Jacinto de Carvalhais",
          neighborhood: "Jardim Santo André",
          house_number: "81",
          state: "São Paulo",
          city: "São Paulo",
          cep: "08390-219",
        },
      },
      {
        id: "524a8719-d7aa-4879-8ed7-a2b172f12eed",
        name: "Aviva Real",
        day: "12/09/2021",
        start_date_time: "10:30",
        end_date_time: "11:30",
        vacancies: "20",
        available_vacancies: "20",
        description: null,
        location: {
          id: "185559b9-edc4-4326-8e9d-e624603f391a",
          name: "Igreja da Graça",
          street: "Padre Jacinto de Carvalhais",
          neighborhood: "Jardim Santo André",
          house_number: "81",
          state: "São Paulo",
          city: "São Paulo",
          cep: "08390-219",
        },
      },
      {
        id: "c6330b25-3b2f-4eec-93fa-ec8218f0572c",
        name: "Missa",
        day: "12/09/2021",
        start_date_time: "10:30",
        end_date_time: "11:30",
        vacancies: "20",
        available_vacancies: "17",
        description: null,
        location: {
          id: "ef58aea9-315e-46ac-90c6-661242df1844",
          name: "Igreja Católica Santo André",
          street: "Padre Jacinto de Carvalhais",
          neighborhood: "Jardim Santo André",
          house_number: "81",
          state: "São Paulo",
          city: "São Paulo",
          cep: "08390-219",
        },
      },
      {
        id: "f7be6b35-766f-4eff-b5e9-afb382a5d861",
        name: "Espirro",
        day: "12/09/2021",
        start_date_time: "10:30",
        end_date_time: "11:30",
        vacancies: "20",
        available_vacancies: "20",
        description: "Evento diário na vida de muitos riniteiros",
        location: {
          id: "185559b9-edc4-4326-8e9d-e624603f391a",
          name: "Igreja da Graça",
          street: "Padre Jacinto de Carvalhais",
          neighborhood: "Jardim Santo André",
          house_number: "81",
          state: "São Paulo",
          city: "São Paulo",
          cep: "08390-219",
        },
      },
    ],
  }),

  components: {
    Footer,
    Header,
    Button,
    // Modal,
    Card,
  },
};
</script>
