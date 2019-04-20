<template>
  <v-app>
    <Navbar/>
    <v-content class="blue-grey lighten-5">
      <router-view></router-view>
    </v-content>
    <Footer/>
  </v-app>
</template>

<script>
import Navbar from "@/components/Navbar.vue";
import Footer from "@/components/Footer.vue";

export default {
  name: "App",
  components: { Navbar, Footer },
  data() {
    return {
      //
    };
  }
};
</script>
