<template>
  <v-app>
    <v-main>
      <Navbar 
        @goToSection="goToSection"
      />
      <Welcome
        id="welcome"
        class="page background--primary"
      />
      <About 
        id="about"
        class="page background--primary"
      />
      <Projects 
        id="projects"
        class="page background--primary"
      />
      <div
        id="contact"
      >
      </div>
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
    Contact,
  },

  data: () => ({
    //
  }),

  methods: {
    goToSection(section) {
      console.log("####", section);
      var selected_section = document.getElementById(section);
      console.log("@@@", selected_section.offset);
      selected_section.scrollIntoView({ behavior: 'smooth'});
    },
  }
};
</script>

<style>
  @import './assets/styles/main.css';
</style>
