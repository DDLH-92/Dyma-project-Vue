<template>
  <Product v-bind="product"/>
</template>

<script setup lang="ts">
import Product from './Product.vue';
import { reactive, ref } from 'vue';
import type { ProductInterface } from './interfaces/product.interface.ts'

const product = reactive<ProductInterface>({
  available: true,
  prix: 1500,
  name: 'Moto'
})

</script>
