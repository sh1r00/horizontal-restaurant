<template>
  <v-navigation-drawer
    v-model="drawer"
    absolute
    temporary
    @input="navDrawerStatus(drawer)"
  >
    <v-list-item>
      <v-list-item-content>
        <v-list-item-title class="title">
          {{ title }}
        </v-list-item-title>
        <v-list-item-subtitle>
          {{ subtitle }}
        </v-list-item-subtitle>
      </v-list-item-content>
    </v-list-item>
    <v-divider />
    <v-list dense nav>
      <div v-for="(item, idx) in items" :key="idx">
        <v-list-item :to="item.link" link exact>
          <v-list-item-content>
            <v-list-item-title>
              {{ item.name }}
            </v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </div>
    </v-list>
  </v-navigation-drawer>
</template>

<script>
export default {
  props: {
    logo: {
      type: String,
      default: 'null',
    },
    toggleDrawer: {
      type: Boolean,
      default: false,
    },
    items: {
      type: Array,
      default: () => [],
    },
  },
  data() {
    return {
      drawer: false,
      title: 'A website',
      subtitle: 'Gna make it especial',
    }
  },
  watch: {
    toggleDrawer() {
      this.drawer = this.$props.toggleDrawer
    },
  },
  methods: {
    navDrawerStatus(value) {
      if (value === false) {
        this.$emit('close-nav-drawer')
      }
    },
  },
}
</script>
