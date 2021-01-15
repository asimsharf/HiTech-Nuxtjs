<template>
  <v-navigation-drawer
    v-model="drawer"
    :mini-variant="miniVariant"
    :clipped="clipped"
    fixed
    app
  >
    <v-list>
      <v-list-item
        v-for="(item, i) in items"
        :key="i"
        :to="item.to"
        router
        exact
      >
        <v-list-item-action>
          <v-icon>{{ item.icon }}</v-icon>
        </v-list-item-action>
        <v-list-item-content>
          <v-list-item-title v-text="item.title" />
        </v-list-item-content>
      </v-list-item>
    </v-list>
  </v-navigation-drawer>
</template>


<script>
export default {
  data() {
    return {
      clipped: true,
      drawer: true,
      fixed: true,
      miniVariant: false,
      items: [
        {
          icon: "mdi-apps",
          title: "الرئيسية",
          to: "/",
        },
        {
          icon: "mdi-lifebuoy",
          title: "المرضى",
          to: "/patients",
        },
        {
          icon: "mdi-chart-bubble",
          title: "العيادات",
          to: "/clinics",
        },
        {
          icon: "mdi-chart-bubble",
          title: "الأطباء",
          to: "/doctors",
        },
        {
          icon: "mdi-chart-bubble",
          title: "الصيدلية",
          to: "/pharmacy",
        },
        {
          icon: "mdi-chart-bubble",
          title: "المخزن",
          to: "/stock",
        },
        {
          icon: "mdi-chart-bubble",
          title: "المعمل",
          to: "/laborator",
        },
        {
          icon: "mdi-chart-bubble",
          title: "الحسابات",
          to: "/accounts",
        },
        {
          icon: "mdi-chart-bubble",
          title: "التقارير",
          to: "/reports",
        },
        {
          icon: "mdi-chart-bubble",
          title: "الإعدادات",
          to: "/settings",
        },
        {
          icon: "mdi-chart-bubble",
          title: "المستخدمين",
          to: "/users",
        },
        {
          icon: "mdi-chart-bubble",
          title: "سجل النشاط",
          to: "/activity",
        },
      ],
      

    };
  },
};
</script>
