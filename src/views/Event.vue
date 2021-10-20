<template>
  <div class="event">
    <v-app>
      <v-main>
        <div class="search">
          <Input @input.native="search($event.target.value)" />
          <Button buttonName="Pesquisar" class="btn" />
        </div>
        <div v-if="filteredItems.length">
          <Card v-for="event in filteredItems" :key="event.id" :event="event" />
        </div>
        <div v-else>
          <Card v-for="event in availableEvents" :key="event.id" :event="event" />
        </div>
      </v-main>
    </v-app>
  </div>
</template>

<script>
import Input from "../components/Input.vue";
import Button from "../components/Button.vue";
import Card from "../components/Card.vue";
import axios from "axios";

export default {
  components: {
    Button,
    Input,
    Card,
  },
  data: () => ({
    events: [],
    filteredItems: [],
  }),
  async mounted() {
    await this.loadEvents();
  },
  methods: {
    async loadEvents() {
      const response = await axios.get("http://localhost:3030/event");
      this.events = response.data;
    },
    search(eventName) {
      const events = this.events.filter((event) => {
        return event.name.toLowerCase().includes(eventName.toLowerCase());
      });
      this.filteredItems = events;
    },
  },
  computed: {
    availableEvents() {
      return this.events
        .filter((event) => event.available_vacancies > 0)
        .sort((a, b) => (a.name > b.name ? 1 : -1));
    },
  },
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
