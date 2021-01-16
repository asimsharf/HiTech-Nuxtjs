<template>
  <v-app-bar color="deep-purple accent-4" :clipped-left="clipped" fixed app>

    <v-app-bar-nav-icon color="white" @click.stop="drawer = !drawer" />

    <v-btn color="white" icon @click.stop="miniVariant = !miniVariant">

      <v-icon color="white"
        >mdi-{{ `chevron-${miniVariant ? "right" : "left"}` }}</v-icon
      >

    </v-btn>

    <v-btn color="white" icon @click.stop="clipped = !clipped">
      <v-icon color="white">mdi-application</v-icon>
    </v-btn>

    <v-btn color="white" icon @click.stop="fixed = !fixed">
      <v-icon>mdi-minus</v-icon>
    </v-btn>

    <v-divider class="mx-4" vertical></v-divider>

    <v-toolbar-title class="title" v-text="title" />

    <v-spacer></v-spacer>

    <v-toolbar-items class="hidden-sm-and-down">
      <v-btn color="white" text> لنك </v-btn>

      <v-divider vertical></v-divider>

      <v-btn color="white" text> لنك </v-btn>

      <v-divider vertical></v-divider>

      <v-btn color="white" text> لنك </v-btn>

      <v-divider vertical></v-divider>
    </v-toolbar-items>

    
  </v-app-bar>
</template>


<script>
export default {
  data() {
    return {
      clipped: true,
      drawer: false,
      fixed: true,
      miniVariant: false,
      title: "HiTech",
    };
  },
};
</script>
<style  scoped>
.title {
  color: white;
}
</style>