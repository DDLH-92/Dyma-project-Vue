<template>
  <Product :prix="1500"/>
</template>

<script setup lang="ts">
import Product from './Product.vue';
import { ref } from 'vue';

const product = ref('moto')

</script>
