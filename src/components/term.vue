<template>
  <v-container fluid>
    <v-row>
      <v-col cols="12">
        <v-combobox
          v-model="normalSelect1"
          :items="items1"
          label=""
          outlined
          dense
        ></v-combobox>
        <v-combobox
          v-model="symbolSelect"
          :items="symbols"
          label=""
          outlined
          dense
        ></v-combobox>
        <v-combobox
          v-model="normalSelect2"
          :items="items2"
          label=""
          outlined
          dense
        ></v-combobox>
        <v-btn id="btn" @click="Onclick()" elevation="2"> Submit </v-btn>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: "term",

  data() {
    return {
      normalSelect1: "选择或输入字段",
      normalSelect2: "选择或输入字段",
      symbolSelect: "选择一个运算符",
      items1: ["Chooose 1", "Chooose 2", "Chooose 3", "Chooose 4"],
      items2: ["Chooose 1", "Chooose 2", "Chooose 3", "Chooose 4"],
      symbols: ["+", "-", "*", "/", "="],
      submit: [],
    };
  },
  props: {},

  methods: {
    Onclick() {
      console.log(this.result);
    },
  },

  computed: {
    result() {
      return this.normalSelect1 + this.symbolSelect + this.normalSelect2;
    },
  },
};
</script>

<style scoped>
.col {
   display: flex;
}
</style>