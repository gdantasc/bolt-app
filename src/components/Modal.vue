<template>
  <div>
    <template>
      <v-row justify="center">
        <v-dialog v-model="dialog" persistent max-width="600px">
          <v-card>
            <div>
              <img src="../assets/logo.png" alt="logo" class="logo-img" />
            </div>
            <div>
              <img
                src="../assets/close.svg"
                alt="logo"
                class="close-img"
                @click="dialog = false"
              />
            </div>
            <v-card-text>
              <v-container>
                <v-row>
                  <v-card-title>
                    <h1>Participe do evento: {{ event.name }}</h1>
                  </v-card-title>
                  <v-col cols="12">
                    <v-text-field
                      label="Nome Completo"
                      type="text"
                      required
                    ></v-text-field>
                  </v-col>
                  <v-col cols="12">
                    <v-text-field label="Email" required></v-text-field>
                  </v-col>
                  <v-col cols="12">
                    <v-text-field
                      label="Apelido"
                      type="text"
                      required
                    ></v-text-field>
                  </v-col>
                </v-row>
              </v-container>
            </v-card-text>
            <v-card-actions>
              <v-spacer></v-spacer>
              <v-btn color="blue darken-1" text @click="dialog = false">
                Salvar
              </v-btn>
            </v-card-actions>
          </v-card>
        </v-dialog>
        <div @click="dialog = true">
      <Button buttonName="Participar" @click="dialog = true" />
        </div>
      </v-row>
    </template>
  </div>
</template>

<script>
import Button from '../components/Button.vue'

export default {
  props: {
    event: {
      type: Object
    }
  },
  components: {
    Button
  },
  data: () => ({
    dialog: false
  }),
  computed: {

  },
  methods: {
  }
};
</script>

<style>
.logo-img {
  width: 80px;
  margin: 10px 0 0 30px;
}

.close-img {
  position: absolute;
  right: 30px;
  top: 30px;
  cursor: pointer;
}
</style>