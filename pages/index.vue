<template>
  <v-container class="grey lighten-5">
    <v-banner two-line>
      <v-avatar slot="icon" color="deep-purple accent-4" size="40">
        <v-icon icon="mdi-lock" color="white"> mdi-lock </v-icon>
      </v-avatar>

      الإحصائيات الخاصه بالعيادة من هنا يتم مراقبه جميع الحركات بداخل العيادة

      <template v-slot:actions>
        <v-btn text color="deep-purple accent-4"> مشاهدة </v-btn>
        <v-btn text color="deep-purple accent-4"> خيار </v-btn>
      </template>
    </v-banner>
    <v-row no-gutters>
      <v-col cols="12" sm="4">
        <v-card class="pa-3"> One of three columns </v-card>
      </v-col>

      <v-col cols="12" sm="4">
        <v-card class="pa-3"> One of three columns </v-card>
      </v-col>

      <v-col cols="12" sm="4">
        <v-card class="pa-3"> One of three columns </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {};
</script>
