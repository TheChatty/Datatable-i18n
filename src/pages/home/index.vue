<script setup lang="ts">
import DataTable from "datatables.net-vue3";
import DataTablesCore from "datatables.net-dt";
import languageDE from "datatables.net-plugins/i18n/de-DE.mjs";

defineOptions({
  name: "Home",
});
DataTable.use(DataTablesCore);
const data = [
  [1, 2],
  [3, 4],
];
const options = {
  language: languageDE,
};
</script>

<template>
  <DataTable :data="data" class="display" :options="options">
    <thead>
      <tr>
        <th>A</th>
        <th>B</th>
      </tr>
    </thead>
  </DataTable>
</template>

<style scoped></style>
