<template>
  <strong>Countries</strong>
  <ul>
    <li v-for="c in countries" :key="c">{{ c }}</li>
  </ul>
  <strong>Users</strong>
  <ul>
    <li v-for="u in users" :key="u.id">{{ u.name }} {{ u.lasName }}</li>
  </ul>
</template>

<script lang="ts" setup>
import { Ref, ref } from "vue";
const countries: Ref<Array<string>> = ref(["México", "USA", "Canada"]);

interface ICountry {
  id: number;
  name: string;
  lasName: string;
}

const users: Ref<Array<ICountry>> = ref([
  {
    id: 1,
    name: "Fernando",
    lasName: "Franco",
  },
  {
    id: 2,
    name: "Brandom",
    lasName: "Cota",
  },
  {
    id: 3,
    name: "Irvi",
    lasName: "Gorgonita",
  },
  {
    id: 4,
    name: "Mangel",
    lasName: "Narco",
  },
]);
</script>
