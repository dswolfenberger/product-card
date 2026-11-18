<script setup lang="ts">
import CardButton from './cardButton.vue'

defineProps<{
  name: string
  price: number
}>()
</script>
<template>
  <article class="product-card">
    <h2>{{ name }}</h2>
    <h3>Starting at ${{ price.toFixed(2) }}</h3>
    <img src="https://placehold.co/300x300" alt="Product image" />
    <p>Some details about the product can be long and cause issues with card alignment so we wan't to truncate it to keep the card easy to take in</p>
    <CardButton :product-name="name" />
  </article>
</template>

<style scoped>
.product-card {
  container-type: inline-size;
  display: grid;
  grid-template-columns: minmax(0, 1fr);
  grid-template-rows: auto auto auto 1fr auto;
  background: #1e1e1e;
  color: white;
  border-radius: 0.8rem;
  width: 100%;
  min-width: 0;
  min-height: 24rem;
  overflow: hidden;
  padding: 0 1rem 1rem;
  box-sizing: border-box;
}

.product-card p {
  align-self: start;
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-line-clamp: 2;
  line-clamp: 2;
  overflow: hidden;
  text-overflow: ellipsis;
}

.product-card img {
  display: block;
  width: 100%;
  height: auto;
  border-radius: 0.6rem;
}

.product-card h2 {
  margin: 0.8rem 0 0 0;
  font-size: 1.2rem;
}

.product-card h3 {
  font-weight: 400;
  margin: 0.4rem 0 0.8rem 0;
  font-size: minmax(1rem 2rem);
  white-space: wrap;
}
</style>
