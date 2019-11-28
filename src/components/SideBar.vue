<template>
  <v-navigation-drawer app clipped>
    <v-list dense>
      <v-list-item @click.stop="navigatePage('HomeContent')">
        <v-list-item-action>
          <v-icon>mdi-home</v-icon>
        </v-list-item-action>
        <v-list-item-content>
          <v-list-item-title>Home</v-list-item-title>
        </v-list-item-content>
      </v-list-item>
      <v-list-item @click.stop="navigatePage('ContactMail')">
        <v-list-item-action>
          <v-icon>mdi-contact-mail</v-icon>
        </v-list-item-action>
        <v-list-item-content>
          <v-list-item-title>
            Material Design Icons
          </v-list-item-title>
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
