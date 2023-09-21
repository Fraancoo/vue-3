<template>
  <h3>{{ counter }}</h3>
  <button @click="addCounter">Incrementar</button>
</template>

<script lang="ts">
// ------ Option API ----------
import { defineComponent } from "vue";
export default defineComponent({
  name: "CounterOption",
  // component: {} <-- Otros componentes que se utilicen
  data() {
    let counter = 0;
    return { counter };
  },
  methods: {
    addCounter(): void {
      this.counter++;
    },
  },
  created() {
    this.counter++;
    console.log(`Created : ${this.counter}`);
  },
  mounted() {
    this.counter++;
    console.log(`Mounted : ${this.counter}`);
  },
  updated() {
    console.log(`Updated : ${this.counter}`);
  },
});
// -----------------
</script>
