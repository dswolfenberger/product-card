<script setup lang="ts">
defineProps<{ productName: string }>()
</script>

<template>
  <button type="button" class="card-button">
    <span class="full-label">Shop {{ productName }}</span>
    <span class="short-label">
      Shop now<span class="product-context"> for {{ productName }}</span>
    </span>
  </button>
</template>

<style scoped>
.card-button {
  background: red;
  color: white;
  border-radius: 0.4rem;
  border-style: none;
  width: 100%;
  height: auto;
  min-height: 3rem;
  padding: 0.5rem 0.25rem;
  font-size: 1rem;
  font-weight: 600;
  line-height: 1.25;
  white-space: nowrap;
  transition: background-color .325s ease;

  &:hover {
    cursor: pointer;
    background: darkred;
  }

}

.short-label {
  display: none;
}

.product-context {
  position: absolute;
  width: 1px;
  height: 1px;
  overflow: hidden;
  clip-path: inset(50%);
  white-space: nowrap;
}

@container (width < 14rem) {
  .full-label {
    display: none;
  }

  .short-label {
    display: inline;
  }
}
</style>
