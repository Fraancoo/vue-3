<template>
  <form>
    <div :style="divForm">
      <label>Email</label>
      <input type="email" />
    </div>
    <div :style="divForm">
      <label>Password</label>
      <input type="password" />
    </div>
  </form>
  <p
    :style="{ userSelect: 'none' }"
    :class="{ danger: hasError }"
    @click="handleClick()"
  >
    Click Me!
  </p>
</template>

<script lang="ts" setup>
import { Ref, ref } from "vue";

let divForm = { marginBottom: "10px", display: "grid", gap: "10px" };
let hasError: Ref<boolean> = ref(false);

const handleClick = () => {
  hasError.value = !hasError.value;
};
</script>

<style>
.danger {
  color: red;
}
</style>
