<template>
  <div
    id="about"
  >
    <v-container>
      <v-row
        class="ml-10"
      >
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
                  TOOLING
                </span>
              </v-container>
            </v-col>
          </v-row>
        </v-col>
      </v-row>
      <v-row>
        <v-col
          class="animate-slide-fade-right"
        >
          <v-row
            class="ml-10 px-10"
          >
            <v-col
              v-for="(tool, index) in tools"
              :key="`tool_${index}`"
              cols="12"
              md="6"
              lg="4"
              class="pt-0 pl-10 d-flex justify-center"
            >
              <p
                class="text--primary mt-5 f18 d-flex"
              >
                <img
                  :src="tool.logo"
                  :alt="tool.name"
                  width="40"
                  class="mr-1"
                >
                <span
                  class="d-flex align-center"
                >
                  {{ tool.name }}
                </span>
              </p>
            </v-col>
          </v-row>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
export default {
  data() {
    return {
      animation_list: [{
        caller: "animate-slide-fade-top",
        class: "slide-fade-top"
      }, {
        caller: "animate-slide-fade-right",
        class: "slide-fade-right"
      }],
      tools: [
        {
          name: 'JAVASCRIPT',
          logo: 'src/assets/logo/javascript-logo.svg',
          width: '40',
        },
        {
          name: 'NODE',
          logo: 'src/assets/logo/node-logo.svg',
          width: '40',
        },
        {
          name: 'VUE',
          logo: 'src/assets/logo/vue-logo.svg',
          width: '40',
        },
        {
          name: 'REACT',
          logo: 'src/assets/logo/react-logo.svg',
          width: '40',
        },
        {
          name: 'TYPESCRIPT',
          logo: 'src/assets/logo/typescript-logo.svg',
          width: '40',
        },
        {
          name: 'SASS',
          logo: 'src/assets/logo/sass-logo.svg',
          width: '40',
        },
        {
          name: 'FIGMA',
          logo: 'src/assets/logo/figma-logo.svg',
          width: '40',
        },
        {
          name: 'PHP',
          logo: 'src/assets/logo/php-logo.svg',
          width: '40',
        },
        {
          name: 'RUBY',
          logo: 'src/assets/logo/ruby-logo.svg',
          width: '40',
        },
        {
          name: 'PYTHON',
          logo: 'src/assets/logo/python-logo.svg',
          width: '40'
        },
        {
          name: 'SQL',
          logo: 'src/assets/logo/sql-logo.png',
          width: '40'
        },
        {
          name: 'MONGODB',
          logo: 'src/assets/logo/mongodb-logo.png',
          width: '40'
        }
      ]
    }
  },
  mounted() {
    const about_position = document.getElementById("about").getBoundingClientRect();
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