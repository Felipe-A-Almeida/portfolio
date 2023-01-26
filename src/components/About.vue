<template>
  <div>
    <v-row
      class="ml-10"
    >
      <v-col
       cols="12"
      >
        <v-row
          class="mt-10 text-align-center"
        >
          <v-col>
            <v-container>
              <span
                class="text--secondary f40 mt-10"
              >
                ABOUT ME
              </span>
            </v-container>
          </v-col>
        </v-row>
      </v-col>
    </v-row>
    <v-row>
      <v-col
        cols="6"
        xs="12"
      >
        <v-row
          class="text-align-center mr-10"
        >
          <v-col
            class="pb-0"
          >
            <v-avatar
              size="150"
            >
              <img
                src="@/assets/my_photo.jpg"
                alt="Felipe Almeida"
                height="200"
                id="profile-photo"
              >
            </v-avatar>
          </v-col>
        </v-row>
        <v-row
          class="text-align-center mt-1 mr-10"
        >
          <v-col>
            <v-container>
              <p
                class="text--primary f18"
              >
                Felipe Augusto
              </p>
              <p
                class="text--primary f18"
              >
                23 years old
              </p>
              <p
                class="text--primary f18"
              >
                Brazil
              </p>
            </v-container>
          </v-col>
        </v-row>
        <v-row
          class="mx-10 px-10"
        >
          <v-col>
            <v-container>
              <p
                class="text--primary f18"
              >
                I’m a software engineer with more than 5 years of professional experience.
                My specialty is design and develop web solutions, landing pages and complex
                systems based on pre-established requirements.
              </p>
            </v-container>
          </v-col>
        </v-row>
      </v-col>
      <v-divider 
        vertical
        class="bar--primary"
      />
      <v-col>
        <v-row>
          <v-col
            class="pt-0 pb-2"
          >
            <span
              class="f32 text--primary ml-10"
            >
              TOOLING
            </span>
          </v-col>
        </v-row>
        <v-divider 
          class="bar--secondary my-3"
        />
        <v-row>
          <v-col
            cols="6"
            xs="12"
            class="pt-0 pl-10"
          >
            <p
              class="text--primary mt-5 f18 d-flex"
            >
              <img
                src="@/assets/logo/javascript-logo.svg"
                alt="Javascript"
                width="40"
                class="mr-1"
              >
              <span
                class="d-flex align-center"
              >
                JAVASCRIPT
              </span>
            </p>
            <p
              class="text--primary mt-5 f18 d-flex"
            >
              <img
                src="@/assets/logo/node-logo.svg"
                alt="Node"
                width="40"
                class="mr-1"
              >
              <span
                class="d-flex align-center"
              >
                NODE
              </span>
            </p>
            <p
              class="text--primary mt-5 f18 d-flex"
            >
              <img
                src="@/assets/logo/vue-logo.svg"
                alt="Vue"
                width="40"
                class="mr-1"
              >
              <span
                class="d-flex align-center"
              >
                VUE
              </span>
            </p>
            <p
              class="text--primary mt-5 f18 d-flex"
            >
              <img
                src="@/assets/logo/react-logo.svg"
                alt="React"
                width="40"
                class="mr-1"
              >
              <span
                class="d-flex align-center"
              >
                REACT
              </span>
            </p>
            <p
              class="text--primary mt-5 f18 d-flex"
            >
              <img
                src="@/assets/logo/typescript-logo.svg"
                alt="Typescript"
                width="40"
                class="mr-1"
              >
              <span
                class="d-flex align-center"
              >
                TYPESCRIPT
              </span>
            </p>
            <p
              class="text--primary mt-5 f18 d-flex"
            >
              <img
                src="@/assets/logo/sass-logo.svg"
                alt="Sass"
                width="40"
                class="mr-1"
              >
              <span
                class="d-flex align-center"
              >
                SASS
              </span>
            </p>
            <p
              class="text--primary mt-5 f18 d-flex"
            >
              <img
                src="@/assets/logo/figma-logo.svg"
                alt="Figma"
                width="35"
                class="mr-1"
              >
              <span
                class="d-flex align-center"
              >
                FIGMA
              </span>
            </p>
          </v-col>
          <v-col
            cols="6"
            xs="12"
            class="pt-0"
          >
            <p
              class="text--primary mt-5 f18 d-flex"
            >
              <img
                src="@/assets/logo/php-logo.svg"
                alt="PHP"
                width="40"
                class="mr-1"
              >
              <span
                class="d-flex align-center"
              >
                PHP
              </span>
            </p>
            <p
              class="text--primary mt-5 f18 d-flex"
            >
              <img
                src="@/assets/logo/ruby-logo.svg"
                alt="Ruby"
                width="40"
                class="mr-1"
              >
              <span
                class="d-flex align-center"
              >
                RUBY
              </span>
            </p>
            <p
              class="text--primary mt-5 f18 d-flex"
            >
              <img
                src="@/assets/logo/python-logo.svg"
                alt="Python"
                width="40"
                class="mr-1"
              >
              <span
                class="d-flex align-center"
              >
                PYTHON
              </span>
            </p>
            <p
              class="text--primary mt-5 f18 d-flex"
            >
              <img
                src="@/assets/logo/sql-logo.png"
                alt="Sql"
                width="40"
                class="mr-1"
              >
              <span
                class="d-flex align-center"
              >
                SQL
              </span>
            </p>
            <p
              class="text--primary mt-5 f18 d-flex"
            >
              <img
                src="@/assets/logo/mongodb-logo.png"
                alt="Mongodb"
                width="40"
                class="mr-1"
              >
              <span
                class="d-flex align-center"
              >
                MONGODB
              </span>
            </p>
          </v-col>
        </v-row>
      </v-col>
    </v-row>
  </div>
</template>

<script>
export default {
  
}
</script>