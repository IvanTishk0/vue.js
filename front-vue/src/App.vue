<script setup>
  import css from "./App.module.css";
  import {ref, reactive, watch} from "vue";
  import Table from "./components/Table/Table.vue";

  const tables = ref(["table1", "table2", "table3", "table4"])


</script>

<template>
  <div v-for="table in tables">
    <Table>{{table}}</Table>
  </div>
</template>


