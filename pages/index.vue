<template>
  <v-layout>
    <v-col class="pa-0" tag="section">
      <vuetify-carousel :items="carousel.home" />
      <v-col class="text-center">
        <h1 class="my-12">something about home</h1>
        <h5 class="mb-4">subtitle it</h5>
      </v-col>
    </v-col>
  </v-layout>
</template>

<script>
import VuetifyCarousel from '~/components/VuetifyCarousel.vue'

export default {
  components: {
    VuetifyCarousel,
  },
  data() {
    return {
      carousel: {
        home: [
          {
            title: 'Random Store',
            src: '/pics/random-store.jpg',
          },
          {
            title: 'Store Front',
            src: '/pics/store-front.jpg',
          },
          {
            title: 'Store',
            src: '/pics/stores.jpg',
          },
        ],
      },
    }
  },
}
</script>
