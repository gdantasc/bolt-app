<template>
  <div>
    <template>
      <v-row justify="center">
        <v-dialog v-model="dialog" persistent max-width="600px">
          <template v-slot:activator="{ on, attrs }">
            <Button buttonName="Participar" v-bind="attrs" v-on="on" />
            </template>
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
                    <h1>Participe de um evento</h1>
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
      </v-row>
    </template>
  </div>
</template>

<script>
import Button from './Button.vue'
export default {
  components:{ Button},
  props: {},
  data: () => ({
    dialog: false,
  }),
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