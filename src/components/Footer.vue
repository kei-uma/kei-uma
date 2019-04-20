<template>
  <v-footer dark height="auto">
    <v-card class="flex" flat tile>
      <v-card-title class="grey darken-1">
        <strong class="subheading">Get connected with us on social networks!</strong>

        <v-spacer></v-spacer>
        <div v-for="i in items" :key="i.id">
          <v-btn :href="i.link[0]" class="mx-3" dark icon>
            <v-icon size="24px">{{ i.icon[0] }}</v-icon>
          </v-btn>
        </div>
      </v-card-title>

      <v-card-actions class="grey darken-4 justify-center">
        &copy;2018 —
        <strong>Vuetify</strong>
      </v-card-actions>
    </v-card>
  </v-footer>
</template>

<script>
export default {
  data: () => ({
    items: [
      {
        id: 1,
        icon: ["fab fa-facebook"],
        link: ["/"]
      },
      {
        id: 2,
        icon: ["fab fa-twitter"],
        link: ["https://twitter.com/KU5353"]
      },
      {
        id: 3,
        icon: ["fab fa-github"],
        link: ["https://github.com/kei-uma/"]
      }
    ]
    // icon: ["fab fa-facebook", "fab fa-twitter", "fab fa-github"],
    // link: ["", "https://twitter.com/KU5353", "https://github.com/kei-uma/"]
  })
};
</script>
