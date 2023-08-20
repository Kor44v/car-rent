<template>
  <div class="shadow">
    <h3 class="mb-5">Agenda el automóvil que necesitas!</h3>

    <v-row>
      <v-col class="d-flex flex-wrap gap">
        <label for=""></label>
        <v-select :items="cars" label="Selecciona el auto" solo></v-select>
        <v-select
          :items="pick"
          label="Elige el punto de recogida"
          solo
        ></v-select>
        <v-select
          :items="drop"
          label="Elige el punto de devolución"
          solo
        ></v-select>
      </v-col>
    </v-row>
    <v-row>
      <v-col class="d-flex">
        <v-menu
          v-model="menu1"
          :close-on-content-click="false"
          :nudge-right="40"
          transition="scale-transition"
          offset-y
          min-width="auto"
        >
          <template v-slot:activator="{ on, attrs }">
            <v-text-field
              v-model="date1"
              label="Fecha de recogida"
              prepend-icon="mdi-calendar"
              readonly
              v-bind="attrs"
              v-on="on"
            ></v-text-field>
          </template>
          <v-date-picker
            color="light-green lighten-2"
            v-model="date1"
            @input="menu1 = false"
          ></v-date-picker>
        </v-menu>
        <v-menu
          v-model="menu2"
          :close-on-content-click="false"
          :nudge-right="40"
          transition="scale-transition"
          offset-y
          min-width="auto"
        >
          <template v-slot:activator="{ on, attrs }">
            <v-text-field
              v-model="date2"
              label="Fecha de devolución"
              prepend-icon="mdi-calendar"
              readonly
              v-bind="attrs"
              v-on="on"
            ></v-text-field>
          </template>
          <v-date-picker
            color="light-green lighten-2"
            v-model="date2"
            @input="menu2 = false"
          ></v-date-picker>
        </v-menu>
        <v-btn color="light-green lighten-2">Buscar</v-btn>
      </v-col>
    </v-row>
  </div>
</template>

<script>
export default {
  name: "book-car",
  created() {},
  data() {
    return {
      cars: ["Volkswagen Golf gti", "Audi RS 3", "Mazda CX-5"],
      pick: ["Santiago", "Rancagua", "Viña del Mar"],
      drop: ["Santiago", "Rancagua", "Viña del Mar"],
      date1: new Date(Date.now() - new Date().getTimezoneOffset() * 60000)
        .toISOString()
        .substr(0, 10),

      menu1: false,
      date2: new Date(Date.now() - new Date().getTimezoneOffset() * 60000)
        .toISOString()
        .substr(0, 10),

      menu2: false,
    };
  },
  props: {},
  methods: {},
};
</script>

<style scoped>
.shadow {
  box-shadow: rgba(100, 100, 111, 0.2) 0px 7px 29px 0px;
  padding: 1rem;
}
.gap {
  gap: 1rem;
}
</style>
