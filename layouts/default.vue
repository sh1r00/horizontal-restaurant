<template>
  <v-app dark>
    <app-nav-bar
      :items="items"
      :logo="logo.path"
      @toggle-nav-drawer="toggleDrawer = !toggleDrawer"
    />
    <app-nav-drawer
      :items="items"
      :logo="logo.path"
      :toggle-drawer="toggleDrawer"
      @close-nav-drawer="toggleDrawer = false"
    />
    <v-main>
      <v-container fluid class="pa-0">
        <nuxt />
      </v-container>
    </v-main>
    <v-footer app>
      <span>&copy; {{ new Date().getFullYear() }}</span>
    </v-footer>
  </v-app>
</template>

<script>
import AppNavBar from '~/components/AppNavBar'
import AppNavDrawer from '~/components/AppNavDrawer'

export default {
  components: {
    AppNavBar,
    AppNavDrawer,
  },
  data() {
    return {
      logo: {
        path: '',
      },
      toggleDrawer: false,
      items: [
        {
          name: 'Home',
          link: '/',
        },
        {
          name: 'About',
          link: '/about',
        },
        {
          name: 'Menu',
          link: '/menu',
        },
        {
          name: 'Contact Us',
          link: '/contact',
        },
        {
          name: 'Press',
          link: '/press',
        },
      ],
    }
  },
}
</script>
