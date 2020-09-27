<template>
  <v-app id="inspire">
    <NavBar :items="items" v-model="drawer" />

    <v-app-bar app color="indigo" dark>
      <v-app-bar-nav-icon @click.stop="drawer = !drawer"></v-app-bar-nav-icon>
      <v-toolbar-title>Drone IQ</v-toolbar-title>
    </v-app-bar>

    <v-main>
      <router-view />
    </v-main>
    <v-footer color="indigo" app>
      <span class="white--text">&copy; {{ new Date().getFullYear() }}</span>
    </v-footer>
  </v-app>
</template>

<script>
import NavBar from "@/components/NavBar.vue";
export default {
  props: {
    source: String,
  },
  components: {
    NavBar,
  },
  data: () => ({
    drawer: null,
    items: [
      {
        icon: "home",
        text: "Home",
        route: "/",
      },
    ],
  }),
};
</script>
