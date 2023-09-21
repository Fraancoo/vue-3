<template>
  <div class="post_container">
    <PostCard />
    <PostCard />
    <PostCard />
    <PostCard />
  </div>
</template>

<script lang="ts" setup>
import PostCard from "./PostCard.vue";
</script>

<style>
.post_container {
  display: grid;
  gap: 15px;
}
</style>
