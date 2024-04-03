<template>
  <div>
    <ul class="background-all">
      <li
        v-for="n in 50"
        :key="n"
      >
      </li>
    </ul>
    <v-row
      class="ml-10 max-width-1900"
    >
      <v-col
       cols="12"
       xl="6"
       lg="6"
       md="6"
      >
        <v-row
          class="slide-fade-bottom"
        >
          <v-col>
            <v-container>
              <span
                class="text--primary f64"
              >
                WELCOME
              </span>
            </v-container>
          </v-col>
        </v-row>
        <v-row
          class="slide-fade-bottom"
        >
          <v-col>
            <v-container>
              <span
                class="text--primary f32"
              >
                My name is Felipe Almeida.
              </span>
            </v-container>
          </v-col>
        </v-row>
        <v-row
          class="slide-fade-right"
        >
          <v-col
            class="m-padding-left-0"
          >
            <v-container
              class="m-padding-left-0"
            >
              <p
                class="text--primary f18 pr-3 pl-2"
              >
                I’m a fullstack developer with more than 5 years of professional experience.
                My specialty is design and develop web solutions, landing pages and complex
                systems based on pre-established requirements. I'm 23 years old and based in Brazil.
              </p>
            </v-container>
          </v-col>
        </v-row>
      </v-col>
      <v-col>
        <div
          class="text-align-center mr-10 pr-10 slide-fade-right mb-5"
        >
          <v-row>
            <v-col>
              <v-avatar
                size="300"
                class="avatar"
              >
                <img
                  src="@/assets/my_photo.jpg"
                  alt="Felipe Almeida"
                  height="400"
                  id="profile-photo"
                >
              </v-avatar>
            </v-col>
          </v-row>
        </div>
      </v-col>    
    </v-row>
  </div>
</template>

<script>
export default {
  
}
</script>