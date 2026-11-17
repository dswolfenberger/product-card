<script setup lang="ts">
import ProductCard from './components/productCard.vue'
import { products } from './components/productName'
</script>

<template>
  <h1 class="primary-title">Upgrade Your Station</h1>
  <div class="product-card--grid">
    <ProductCard v-for="product in products" :key="product.id" :name="product.name"/>
  </div>
</template>

<style>
body {
  font-family: Arial, Helvetica, sans-serif;
  display: flex;
  align-items: center;
  justify-content: center;
  margin: 10rem;
}

.product-card--grid {
  display: flex;
  flex-direction: row;
  gap: 1rem;
}

.primary-title {
  max-width: 50%;
}
</style>
