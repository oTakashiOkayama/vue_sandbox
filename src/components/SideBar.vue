<template>
  <v-navigation-drawer app clipped>
    <v-list dense>
      <v-list-item @click.stop="navigatePage('HomeContent')">
        <v-list-item-action>
          <v-icon>home</v-icon>
        </v-list-item-action>
        <v-list-item-content>
          <v-list-item-title>Home</v-list-item-title>
        </v-list-item-content>
      </v-list-item>
      <v-list-item @click.stop="navigatePage('ContactMail')">
        <v-list-item-action>
          <v-icon>contact_mail</v-icon>
        </v-list-item-action>
        <v-list-item-content>
          <v-list-item-title>Contact</v-list-item-title>
        </v-list-item-content>
      </v-list-item>
    </v-list>
  </v-navigation-drawer>
</template>

<script>
export default {
  name: 'SideBar',

  props: {
    putDrawer: Boolean,
  },

  data: () => ({
    drawer: true,
  }),

  computed: {
    calcDrawer: function() {
      return this.putDrawer || this.drawer
    },
  },

  methods: {
    navigatePage: function(page) {
      this.$router.push(page)
    },
  },
}
</script>
