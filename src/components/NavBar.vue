<template>
  <v-app-bar app clipped-left dark color="red">
    <v-app-bar-nav-icon v-if="user" @click="drawer ? hideDrawer() : showDrawer()" />
    <v-toolbar-title class="font-weight-light">
      <span>Movies</span>
    </v-toolbar-title>
  </v-app-bar>
</template>

<script>
import { mapGetters, mapActions } from 'vuex'
export default {
  name: 'NavBar',
  computed: {
    ...mapGetters({
      drawer: 'getDrawer',
      user: 'getUser',
    }),
  },
  methods: {
    ...mapActions(['hideDrawer', 'showDrawer']),
  },
}
</script>