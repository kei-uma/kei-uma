<template>
  <div class="home">
    <v-card flat app>
      <v-card-text
        style="white-space: pre-line"
        class="display-1 blue-grey lighten-5"
      >{{ card_text }}</v-card-text>
    </v-card>
  </div>
</template>

<<script>
export default {
  data() {
    return {
      card_text: `こんにちは!
      Keisukeです。
      
      `,
      card_text_en: `I'm Keisuke.
      Thank you for comming to my page.
      I've majored in computer sience for four yaers.
      I am researching about activity recognition using non-contact sensors.
      I wanna make people's lives prosperous without making computers conscious in the future.
      `
    };
  }
};
</script>

<style>
.home {
  margin: 0 auto;
  margin-top: 30px;
  max-width: 767px;
}
</style>