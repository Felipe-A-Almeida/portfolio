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
            v-for="n in 25"
            :key="n"
            v-slot="{ active, toggle }"
          >
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