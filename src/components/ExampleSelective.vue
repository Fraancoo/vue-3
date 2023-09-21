<template>
  <h1>Edad: {{ age }}</h1>
  <!-- vIf -->
  <p v-if="age < 18">Eres menor de edad</p>
  <p v-else>Eres mayor de edad</p>
  <!--
    Con vIf, la condición que no se cumpla
    no se mostrará en el DOM.
    Esta condición hace un DOM más limpio
  -->

  <!-- vShow -->
  <p v-show="age < 18">Eres menor de edad</p>
  <p v-show="age > 18">Eres mayor de edad</p>
  <!--
    Con vShow, la condición que no se cumpla
    se mostrará en el DOM con la propiedad
    display: none
    Esta condición hace un renderizado más rápido
  -->
</template>

<script lang="ts" setup>
let age = 10;
</script>
