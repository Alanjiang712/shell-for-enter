<template>
  <v-app>
    <v-container>
      <term />
      <term :key="index" v-for="(item, index) in terms" />
      <addBtn @generateID="radomID()" />
    </v-container>
  </v-app>
</template>

<script>
//修改测试
import term from "./components/term.vue";
import addBtn from "./components/addBtn.vue";

export default {
  name: "App",

  components: {
    term,
    addBtn,
  },

  data() {
    return {
      terms: [],
    };
  },
  methods: {
    radomID() {
      this.terms.push(Date.now());
      console.log(Date.now());
    },
  },
};
</script>

<style scoped>
#btn {
  width: 150px;
  display: flex;
}
</style>