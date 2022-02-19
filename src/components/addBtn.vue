<template>
  <v-btn @click="generateID()" elevation="2" icon>
    <v-icon> mdi-plus </v-icon>
  </v-btn>
</template>

<script>
export default {
  name: "addBtn",

  methods: {
    generateID() {
      this.$emit('generateID')
    }
  },
};
</script>

<style scoped>
.v-btn {
  display: flex;
}
</style>