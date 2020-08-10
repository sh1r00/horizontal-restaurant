<template>
  <v-app-bar flat color="primary" class="pa-0" shrink-on-scroll prominent app>
    <v-btn width="80px" height="40px" text to="/">
      <v-img
        width="80px"
        height="40px"
        :src="`http://localhost/mysites/${logo}`"
      />
    </v-btn>
    <v-spacer />
    <v-toolbar-items class="hidden-sm-and-down pa-0">
      <div v-for="(item, idx) in items" :key="idx">
        <v-btn text :to="item.link" link exact class="secondary--text">
          {{ item.name }}
        </v-btn>
      </div>
    </v-toolbar-items>
    <v-spacer />
    <v-app-bar-nav-icon
      color="secondary"
      class="hidden-md-and-up"
      @click="toggleNavDrawer"
    />
  </v-app-bar>
</template>
<script>
export default {
  props: {
    logo: {
      type: String,
      default: 'null',
    },
    items: {
      type: Array,
      default: () => [],
    },
  },
  methods: {
    toggleNavDrawer() {
      this.$emit('toggle-nav-drawer')
    },
  },
}
</script>
