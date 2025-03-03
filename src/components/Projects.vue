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
      class="project-ml  mb-5"
    >
      <v-col>
        <v-slide-group
          multiple
          show-arrows
        >
          <v-slide-item
            class="project-card-item ml-3"
          >
            <v-card
              class="project-ml project-card m-margin-left-0 center"
            >
              <img
                class="white--text align-end project-img"
                height="200"
                src="@/assets/project-gpt3.png"
              />
              <v-card-subtitle class="mt-5 pb-0">
                <span class="f24">GPT-3  Showcase</span>
              </v-card-subtitle>

              <v-card-text class="text--primary">
                <div
                  class="left"
                >
                  A landing page about GPT-3, the cutting-edge AI language
                  model revolutionizing industries worldwide. Learn more about its capabilities,
                  applications, and how it can transform your projects. Dive into the future
                  of AI-driven innovation!".
                </div>
                <div
                  class="left"
                >
                  This project was developed using ReactJS framework.
                </div>
              </v-card-text>

              <v-card-actions>
                <a
                  href="https://felipe-a-almeida.github.io/react_project/"
                  target="_blank"
                >
                  <v-btn
                    color="var(--secondary-color)"
                    text
                  >
                    Open
                  </v-btn>
                </a>
                <a
                  href="https://felipe-a-almeida.github.io/react_project/"
                  target="_blank"
                >
                  <v-btn
                    color="var(--secondary-color)"
                    text
                  >
                    Github
                  </v-btn>
                </a>
              </v-card-actions>
            </v-card>
          </v-slide-item>
          <v-slide-item
            class="project-card-item"
          >
            <v-card
              class="project-ml project-card m-margin-left-0 center"
            >
              <img
                class="white--text align-end project-img"
                height="200"
                src="@/assets/project-anama.png"
              />
              <v-card-subtitle class="mt-5 pb-0">
                <span class="f24">Anamá Restaurant</span>
              </v-card-subtitle>

              <v-card-text class="text--primary">
                <div
                  class="left"
                >
                  Landing page to this refined restaurant. Founded by chef Maria Laura, from Ipeúna/SP - Brazil, this experience will bring the flavors and passion of her country. Certainly you will require a comeback.
                </div>
                <div
                  class="left"
                >
                  This project was developed using VueJs and Vuetify framework.
                </div>
              </v-card-text>

              <v-card-actions>
                <a
                  href="https://felipe-a-almeida.github.io/anama_restaurant/"
                  target="_blank"
                >
                  <v-btn
                    color="var(--secondary-color)"
                    text
                  >
                    Open
                  </v-btn>
                </a>

                <a
                  href="https://github.com/Felipe-A-Almeida/anama_restaurant"
                  target="_blank"
                >
                  <v-btn
                    color="var(--secondary-color)"
                    text
                  >
                    Github
                  </v-btn>
                </a>
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