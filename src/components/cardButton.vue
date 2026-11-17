<script setup lang="ts">
defineProps<{ productName: string }>()
</script>

<template>
  <button type="button" class="card-button">
    Shop {{ productName }}
  </button>
</template>

<style scoped>
.card-button {
  background: red;
  color: white;
  border-radius: 0.4rem;
  border-style: none;
  width: 100%;
  height: 3rem;
  font-size: 0.9rem;
  transition: all 1s ease-out;

  &:hover {
    cursor: pointer;
    background: darkred;
  }
}
</style>
