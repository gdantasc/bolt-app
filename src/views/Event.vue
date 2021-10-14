<template>
  <div class="event">
    <v-app>
      <v-main>
        <div class="search">
          <Input />
          <Button buttonName="Pesquisar" class="btn" />
        </div>
        <Card v-for="event in filteredEvents" :key="event" :event="event" />
      </v-main>
    </v-app>
  </div>
</template>

<script>
import Input from "../components/Input.vue";
import Button from "../components/Button.vue";
import Card from "../components/Card.vue";
import axios from 'axios'

export default {
  components: {
    Button,
    Input,
    Card,
  },
  data: () => ({
    events: [],
  }),
  async mounted() {
    await this.loadEvents()
  },
  methods: {
    async loadEvents() {
        const response = await axios.get('http://localhost:3030/event')
        console.log(response.data)
        this.events = response.data
    }
  },
  computed: {
    filteredEvents() {
      return this.events.filter(event => event.available_vacancies > 0).sort((a, b) => a.name > b.name ? 1 : -1)
    }
  }
};
</script>
<style scoped>
.search {
  display: flex;
  margin: 1% 15.5%;
}
.btn {
  margin-left: 30px;  
}
</style>
