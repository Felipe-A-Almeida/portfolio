<template>
  <v-app>
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
        class="page background--primary px-10"
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
      <Activity
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
import Activity from "./components/Activity/index.vue";
import Projects from "./components/Projects.vue";
import Contact from "./components/Contact.vue";
import Footer from "@/components/Footer.vue";

export default {
  name: "App",

  components: {
    Navbar,
    Welcome,
    About,
    Activity,
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
