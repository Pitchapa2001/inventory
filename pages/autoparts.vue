<template>
  <v-col cols="12" sm="10" md="4">
    <v-text-field
      label="Filled"
      placeholder="Dense & Rounded"
      filled
      rounded
      dense
    >
    </v-text-field>
    <v-btn elevation="2"> ค้นหา</v-btn>
    <v-btn elevation="2"> เพิ่มข้อมูลอะไหล่</v-btn>
    <v-data-table
      :headers="headers"
      :items="theemployee"
      :items-per-page="5"
      class="elevation-2"
      density="compact"
      item-key="name"
    >
    </v-data-table>
  </v-col>
</template>

<script>
export default {
  data() {
    return {
      headers: [
        {
          text: "No.",
          align: "numbers",
          sortable: false,
          value: "name",
        },
        { text: "หมายเลขอะไหล่", value: "partscode" },
        { text: "รายการ", value: "listed" },
        { text: "จำนวน", value: "number" },
        { text: "เลือก", value: "choose" },
      ],
      theemployee: [],
    };
  },
};
</script>