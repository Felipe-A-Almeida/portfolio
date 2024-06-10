<template>
  <div>
    <v-app-bar
      color="black accent-4"
      dense
      dark
      class="px-5"
      style="width: 100vw"
    >

      <template 
        v-if="$vuetify.display.mobile"
        v-slot:append
      >
        <v-menu>
          <template v-slot:activator="{ props }">
            <v-btn icon="mdi-menu" v-bind="props"></v-btn>
          </template>

          <v-list
            class="py-0"
          >
            <v-list-item
              v-for="item in menu_items"
              :key="`mobile_item_${item.label}`"
              class="responsive-menu-item px-10"
              @click="$emit('goToSection', item.link)"
            >
              <span
                color="white"
              >
                {{ item.label }}
              </span>
            </v-list-item>
          </v-list>
        </v-menu>
      </template>
      <div
        v-if="!$vuetify.display.mobile"
      >
        <v-btn
          v-for="item in menu_items"
          :key="`item_${item.label}`"
          @click="$emit('goToSection', item.link)"
        >
          <span
            color="white"
          >
            {{ item.label }}
          </span>
        </v-btn>
      </div>
    </v-app-bar>
  </div>
</template>

<script>
export default {
  name: "Navbar",

  data() {
    return {
      menu_items: [
        {
          label: "WELCOME",
          link: "welcome",
        },
        {
          label: "ABOUT",
          link: "about",
        },
        {
          label: "ACTIVITIES",
          link: 'activities'
        },
        {
          label: "PROJECTS",
          link: "projects",
        },
        {
          label: "CONTACT",
          link: "contact",
        },
      ]
    }
  }
};
</script>
