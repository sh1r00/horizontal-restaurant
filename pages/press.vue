<template>
  <v-layout>
    <v-col tag="section" class="text-center">
      <h1 class="my-12">Press</h1>
      <v-row wrap>
        <v-card v-for="(item, idx) in articles" :key="idx" class="ma-6">
          <v-card-text>
            <a :href="item.link">
              <v-img height="200px" max-width="200px" :src="item.img" />
            </a>
          </v-card-text>
          <v-card-title>
            <a :href="item.link">
              {{ item.title }}
            </a>
          </v-card-title>
          <v-card-subtitle class="mt-1">
            {{ item.subtitle }}
          </v-card-subtitle>
        </v-card>
      </v-row>
    </v-col>
  </v-layout>
</template>

<script>
export default {
  data() {
    return {
      articles: [
        {
          title: 'article 1',
          subtitle: 'Some kinda aricle',
          img: '/pics/lamp-logo.jpg',
          link: '#',
        },
        {
          title: 'article 2',
          subtitle: 'Some kinda aricle',
          img: '/pics/chair-logo.jpg',
          link: '#',
        },
        {
          title: 'article 3',
          subtitle: 'Some kinda aricle',
          img: '/pics/espresso.jpg',
          link: '#',
        },
        {
          title: 'article 4',
          subtitle: 'Some kinda aricle',
          img: '/pics/coffee.jpg',
          link: '#',
        },
      ],
    }
  },
}
</script>
