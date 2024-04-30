<template>
  <div
    class="text-white activity-card"
  >
    <v-icon
      size="70"
      class="w-100 d-flex justify-center"
    >
      {{ icon }}
    </v-icon>
    <p
      class="f24 w-100 d-flex justify-center mt-2"
    >
      {{ title }}
    </p>
    <v-divider></v-divider>
    <p
      class="mt-3"
    >
      {{  description  }}
    </p>
  </div>
</template>

<script>
export default {
  props: {
    icon: String,
    title: String,
    description: String
  }
}
</script>