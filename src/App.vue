<template>
  <v-app>
    <ul class="background-all">
      <li
        v-for="n in 50"
        :key="n"
      >
      </li>
    </ul>
    <v-main>
      <Navbar 
        @goToSection="goToSection"
      />
      <v-row>
        <v-col
          class="primary-bar bar"
        />
      </v-row>
      <Welcome
        id="welcome"
        class="page background--primary"
      />
      <v-row>
        <v-col
          class="primary-bar bar"
        />
      </v-row>
      <About 
        id="about"
        class="page background--primary"
      />
      <v-row>
        <v-col
          class="primary-bar bar"
        />
      </v-row>
      <Projects 
        id="projects"
        class="page background--primary"
      />
      <v-row>
        <v-col
          class="primary-bar bar"
        />
      </v-row>
      <div
        id="contact"
      >
      </div>
      <Contact
        class="page background--primary"
      />
      <Footer 
        class="footer"
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
import Footer from "@/components/Footer.vue";

export default {
  name: "App",

  components: {
    Navbar,
    Welcome,
    About,
    Projects,
    Contact,
    Footer
  },

  data: () => ({
    //
  }),

  methods: {
    goToSection(section) {
      var selected_section = document.getElementById(section);
      const y = selected_section.getBoundingClientRect().top + window.pageYOffset - 100;
      window.scrollTo({top: y, behavior: 'smooth'});
    },
  }
};
</script>

<style>
  @import './assets/styles/main.css';
  @import './assets/styles/background.css';
</style>
