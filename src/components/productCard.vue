<script setup lang="ts">
import CardButton from './cardButton.vue'

defineProps<{ name: string }>()
</script>
<template>
  <article class="product-card">
    <h2>{{ name }}</h2>
    <img src="https://placehold.co/300x300" alt="Product image" />
    <p>Some details about the product</p>
    <CardButton :product-name="name" />
  </article>
</template>

<style scoped>
.product-card {
  background: #333333;
  color: white;
  border-radius: 0.8rem;
  width: 20rem;
  min-height: 35rem;
  overflow: hidden;
  padding: 0 1rem;
  box-sizing: border-box;
}

.product-card img {
  display: block;
  width: 100%;
  height: auto;
  border-radius: 0.6rem;
}

.product-card h2 {
  margin:0.8rem 0;
}
</style>
