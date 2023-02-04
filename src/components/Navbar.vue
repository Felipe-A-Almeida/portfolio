<template>
  <div>
    <v-app-bar
      color="black accent-4"
      dense
      dark
      class="px-5"
    >
      <v-toolbar-title>LOGO</v-toolbar-title>

      <v-spacer></v-spacer>

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
