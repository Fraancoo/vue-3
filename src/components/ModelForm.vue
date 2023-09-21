<template>
  <form>
    <div>
      <label for="text">Texto</label>
      <input type="text" id="text" autocomplete="off" v-model="inputText" />
    </div>
    <div>
      <input type="checkbox" id="check" v-model="inputBool" />
      <label for="check" :style="{ userSelect: 'none' }">
        Acepto los términos y condiciones
      </label>
    </div>
    <div>
      <label for="select">Countries:</label>
      <select id="select" v-model="inputSelect">
        <option value="1">Canada</option>
        <option value="2">USA</option>
        <option value="3">México</option>
      </select>
    </div>
  </form>
  <strong>{{ inputText }}</strong>
  <br />
  <strong v-if="inputBool">Sí soy amá</strong>
  <br />
</template>

<script lang="ts" setup>
import { Ref, ref } from "vue";
let inputText: Ref<string> = ref("");
let inputBool: Ref<boolean> = ref(false);
let inputSelect: Ref<number> = ref(1);
</script>

<style scoped>
form {
  margin-bottom: 10px;
}

form > div {
  display: flex;
  gap: 0 10px;
}
</style>
