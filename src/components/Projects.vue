<template>
  <div>
    <ul class="background-all">
      <li
        v-for="n in 50"
        :key="n"
      >
      </li>
    </ul>
    <v-row>
      <v-col
       cols="12"
      >
        <v-row
          class="mt-10 text-align-center animate-slide-fade-right"
        >
          <v-col>
            <v-container>
              <span
                class="text--secondary f40 mt-10"
              >
                PROJECTS
              </span>
            </v-container>
          </v-col>
        </v-row>
      </v-col>
    </v-row>
    <v-row
      class="project-ml"
    >
      <v-col>
        <v-slide-group
          multiple
          show-arrows
        >
          <v-slide-item
            v-for="(project, index) in projects"
            :key="`project_${index}`"
          >
            <v-card
              class="project-ml project-card m-margin-left-0"
            >
              <v-img
                class="white--text align-end"
                height="200px"
                :src="project.img"
              />
              <v-card-subtitle class="mt-5 pb-0">
                <span class="f24">{{ project.title }}</span>
              </v-card-subtitle>

              <v-card-text class="text--primary">
                <div>
                  {{ project.description }}
                </div>
                <div>
                  {{ project.details }} 
                </div>
              </v-card-text>

              <v-card-actions>
                <v-btn
                  color="var(--secondary-color)"
                  text
                >
                  Open
                </v-btn>

                <v-btn
                  color="var(--secondary-color)"
                  text
                >
                  Github
                </v-btn>
              </v-card-actions>
            </v-card>
          </v-slide-item>
        </v-slide-group>
      </v-col>
    </v-row>
  </div>
</template>

<script>
export default {
  data(){
    return {
      projects: [{
        img: 'src/assets/project-pokedex.png',
        title: 'Pokedex',
        description: "This software allows you to consult all pokemons using PokeAPI. It also allow you to search for a specific pokemon by it's name and shows details about a selected Pokemon.",
        details: 'This project was developed using VueJs and Vuetify framework.'
      }],
      animation_list: [{
        caller: "animate-slide-fade-top",
        class: "slide-fade-top"
      }, {
        caller: "animate-slide-fade-right",
        class: "slide-fade-right"
      }],
    }
  },
  mounted() {
    const about_position = document.getElementById("projects").getBoundingClientRect();
    window.addEventListener("scroll", (event) => {
      let scroll = window.scrollY;
      if (scroll > about_position.top - 500) {
        this.animation_list.forEach(animation => {
          const divs = document.getElementsByClassName(animation.caller);
          Array.from(divs).forEach((div) => {
            div.classList.add(animation.class);
            div.classList.remove(animation.caller);
          })
        });
      }
    });
  },
}
</script>