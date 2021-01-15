<template>
  <v-app dark>
    <NavigationDrawer />
    <AppBar />
    <v-main>
      <v-container>
        <nuxt />
      </v-container>
    </v-main>

    <Footer />
  </v-app>
</template>

<script>
import Footer from "@/components/Navigation/Footer";
import AppBar from "@/components/Navigation/AppBar";
import NavigationDrawer from "@/components/Navigation/NavigationDrawer";
export default {
  components: {
    Footer,
    AppBar,
    NavigationDrawer,
  },

  methods: {
    changeRTL() {
      this.$vuetify.rtl = true;
    },
  },

  created() {
    this.changeRTL();
  },
};
</script>
