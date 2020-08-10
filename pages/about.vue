<template>
  <v-layout>
    <v-col class="text-center pa-0" tag="section">
      <vuetify-carousel :items="carousel.about" />
      <h1 class="my-12">A little about us</h1>
      <v-col style="margin: 0 10% 0 10%;">
        <v-row style="margin: 4em 30% 2em 0;">
          <v-img
            height="450px"
            max-width="450px"
            :src="aboutImg.top"
            style="margin-right: 5em; border-radius: 6%;"
            alt="About Image Top"
          />
          <p>Something about this picture</p>
        </v-row>
        <v-row style="margin: 4em 0 2em 30%;">
          <p>Something else about this picture</p>
          <v-img
            height="450px"
            max-width="450px"
            :src="aboutImg.bottom"
            style="margin-left: 5em; border-radius: 6%;"
            alt="About Image Bottom"
          />
        </v-row>
      </v-col>
    </v-col>
  </v-layout>
</template>

<script>
export default {
  data() {
    return {
      aboutImg: {
        top: '/pics/restaurant-owner.jpg',
        bottom: '/pics/restaurant-server.jpg',
      },
      carousel: {
        about: [
          {
            title: 'Coffee',
            src: '/pics/coffee.jpg',
          },
          {
            title: 'Sandwich',
            src: '/pics/sandwich.jpg',
          },
          {
            title: 'Table Logo',
            src: '/pics/table-logo.jpg',
          },
        ],
      },
    }
  },
}
</script>
