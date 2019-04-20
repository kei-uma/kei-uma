<template>
  <v-toolbar flat app class="blue-grey lighten-5">
    <v-toolbar-title class="font-weight-black">ku</v-toolbar-title>
    <v-spacer></v-spacer>
    <v-toolbar-items>
      <v-btn @click="ClickEvent('/')" text class="blue-grey lighten-5" outline>Home</v-btn>
      <v-btn @click="ClickEvent('about')" text class="blue-grey lighten-5" outline>About</v-btn>
      <v-btn @click="ClickEvent('work')" text class="blue-grey lighten-5" outline>Work</v-btn>
    </v-toolbar-items>
  </v-toolbar>
</template>

<script>
export default {
  methods: {
    ClickEvent: function(path) {
      console.log(path);
      this.$router.push({ path: path });
    }
  },
  data() {
    return {};
  }
};
</script>
