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
                PROJECTS
              </span>
            </v-container>
          </v-col>
        </v-row>
      </v-col>
    </v-row>
    <v-row>
      <v-col>
        <v-slide-group
          multiple
          show-arrows
        >
          <v-slide-item
            v-for="n in 9"
            :key="n"
          >
            <v-card
              class="mx-10 project-card"
            >
              <v-img
                class="white--text align-end"
                height="200px"
                src="https://cdn.vuetifyjs.com/images/cards/docks.jpg"
              />
              <v-card-subtitle class="mt-5 pb-0">
                <span class="f24">Number 10</span>
              </v-card-subtitle>

              <v-card-text class="text--primary">
                <div>Whitehaven Beach</div>

                <div>Whitsunday Island, Whitsunday Islands</div>
              </v-card-text>

              <v-card-actions>
                <v-btn
                  color="var(--secondary-color)"
                  text
                >
                  Share
                </v-btn>

                <v-btn
                  color="var(--secondary-color)"
                  text
                >
                  Explore
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

}
</script>