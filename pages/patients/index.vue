<template>
  <v-card>
    <v-tabs v-model="tab" background-color="primary" dark>
      <v-tab v-for="item in items" :key="item.tab">
        {{ item.tab }}
      </v-tab>
    </v-tabs>

    <v-tabs-items v-model="tab">
      <v-tab-item v-for="item in items" :key="item.tab">
        <v-card flat>
          <v-card-text>{{ item.content }}</v-card-text>
        </v-card>
      </v-tab-item>
    </v-tabs-items>
  </v-card>
</template>
<script>
export default {
  data() {
    return {
      tab: null,
      items: [
        { tab: "بيانات المريض", content: "بيانات المريض" },
        { tab: "مريض مراجع", content: "مريض مراجع" },
        { tab: "إدارة الفواتير", content: "إدارة الفواتير" },
        { tab: "فواتير المريض", content: "فواتير المريض" },
        { tab: "فواتيري", content: "فواتيري" },
        { tab: "إجمالي الدخل", content: "إجمالي الدخل" },
      ],
    };
  },
};
</script>