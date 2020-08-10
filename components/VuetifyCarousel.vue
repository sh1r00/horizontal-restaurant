<template>
  <v-carousel height="100vh" width="100vw" hide-delimiters :show-arrows="true">
    <v-carousel-item
      v-for="(item, i) in items"
      :key="i"
      :src="item.src"
      :alt="item.title"
    />
  </v-carousel>
</template>

<script>
export default {
  name: 'VuetifyCarousel',
  props: {
    items: {
      type: Array,
      default: () => [],
    },
  },
}
</script>
