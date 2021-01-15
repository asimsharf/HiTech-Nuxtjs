<template>
  <v-footer color="deep-purple accent-4" :absolute="!fixed" app>
    <span color="white">&copy; {{ new Date().getFullYear() }}</span>
  </v-footer>
</template>
<script>
export default {
  data() {
    return {
      fixed: true,
    };
  },
};
</script>
