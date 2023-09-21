<template>
  <div class="card_container">
    <h1>T[itulo]</h1>
    <p>
      Lorem ipsum dolor sit amet consectetur, adipisicing elit. Error esse
      voluptatum, iste voluptatibus facilis impedit a molestias molestiae quis
      accusamus aliquid repellendus eaque, soluta quisquam deleniti. Quia
      dolorem architecto placeat.
    </p>
    <PostButton />
  </div>
</template>

<script lang="ts" setup>
import PostButton from "./PostButton.vue";
</script>

<style scoped>
.card_container {
  padding: 15px;
  border: 1px solid rgba(0, 0, 0, 0.3);
  border-radius: 15px;
  transition: 300ms;
  cursor: pointer;
}

.card_container:hover {
  background-color: thistle;
}
</style>
