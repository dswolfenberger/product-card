<script setup lang="ts">
import ProductCard from './components/productCard.vue'
import { products } from './data/products'
</script>

<template>
  <div class="site-header">
    <h1>Products</h1>
  </div>
  <h2 class="primary-title">Upgrade Your Station</h2>
  <div class="product-card--grid" role="region" aria-label="Products">
    <ProductCard
      v-for="product in products"
      :key="product.id"
      :name="product.name"
      :price="product.price"
    />
  </div>
  <div class="section">
    <h4>Other Stuff</h4>
  </div>
</template>
