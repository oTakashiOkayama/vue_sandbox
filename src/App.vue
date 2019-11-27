<template>
  <v-app id="inspire">
    <SideBar :putDrawer="true" @nav-page="navigatePage" />

    <v-app-bar app clipped-left color="indigo" dark>
      <v-app-bar-nav-icon @click.stop="drawer = !drawer"></v-app-bar-nav-icon>
      <v-toolbar-title>Application</v-toolbar-title>
    </v-app-bar>

    <v-content>
      <router-view></router-view>
    </v-content>

    <v-footer color="indigo" app>
      <span class="white--text">&copy; 2019</span>
    </v-footer>
  </v-app>
</template>

<script>
import SideBar from './components/SideBar'

export default {
  name: 'App',

  components: {
    SideBar,
  },

  methods: {
    navigatePage: function(page) {
      this.currentPage = page
    },
  },

  data: () => ({
    drawer: null,
    currentPage: 'HomeContent',
  }),
}
</script>
