<template>
  <v-app>
    <v-main>
      <Navbar />
      <Welcome
        class="page background--primary"
      />
      <About 
        class="page background--primary"
      />
      <Projects 
        class="page background--primary"
      />
      <Contact
        class="page background--primary"
      />
    </v-main>
  </v-app>
</template>

<script>
import Navbar from "./components/Navbar.vue";
import Welcome from "./components/Welcome.vue";
import About from "./components/About.vue";
import Projects from "./components/Projects.vue";
import Contact from "./components/Contact.vue";

export default {
  name: "App",

  components: {
    Navbar,
    Welcome,
    About,
    Projects,
    Contact
  },

  data: () => ({
    //
  }),
};
</script>

<style>
  @import './assets/styles/main.css';
</style>
