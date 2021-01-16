<template>
  <v-dialog v-model="dialogDelete" max-width="500px">
    <v-card>
      <v-card-title>هل أنت متأكد من عملية الحذف!</v-card-title>
      <v-card-actions>
        <v-spacer></v-spacer>
        <v-btn color="blue darken-1" text @click="closeDelete">إلغاء</v-btn>
        <v-btn color="blue darken-1" text @click="deleteItemConfirm"
          >موافق</v-btn
        >
        <v-spacer></v-spacer>
      </v-card-actions>
    </v-card>
  </v-dialog>
</template>

<script>
export default {
  data: () => ({
    dialog: false,
    dialogDelete: false,
  }),

  methods: {
    closeDelete() {
      this.dialogDelete = false;
      this.$nextTick(() => {
        this.editedItem = Object.assign({}, this.defaultItem);
        this.editedIndex = -1;
      });
    },
    deleteItemConfirm() {
      this.patientsList.splice(this.editedIndex, 1);
      this.closeDelete();
    },
  },
};
</script>