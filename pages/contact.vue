<template>
  <v-layout>
    <v-col class="pa-0" tag="section">
      <vuetify-carousel :items="carousel.contact" />
      <v-col class="text-center">
        <h1 class="my-12">Contact Us</h1>
        <img src="/v.png" alt="Vuetify.js" class="mb-5" />
        <v-card>
          <google-maps />
        </v-card>
        <blockquote class="blockquote">
          &#8220;First, solve the problem. Then, write the code.&#8221;
          <footer>
            <small>
              <em>&mdash;John Johnson</em>
            </small>
          </footer>
        </blockquote>
      </v-col>
    </v-col>
  </v-layout>
</template>
<script>
import GoogleMaps from '~/components/GoogleMaps.vue'
export default {
  components: {
    GoogleMaps,
  },
  data() {
    return {
      carousel: {
        contact: [
          {
            title: 'Alex Loup',
            src: '/pics/alex-loup-397220-unsplash.jpg',
          },
          {
            title: 'Edgar Casrejon',
            src: '/pics/edgar-castrejon-459822-unsplash.jpg',
          },
          {
            title: 'Burger 2',
            src: '/pics/burger2.jpg',
          },
        ],
      },
    }
  },
}
</script>
