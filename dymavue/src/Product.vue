<template>
  <h3>{{ title }}</h3>
</template>

<script lang="ts" setup>
import { computed } from 'vue'
import type { ProductInterface } from './interfaces/product.interface.ts'


const props = defineProps({
 available: boolean,
 prix: number,
 name: string
})

const title = computed(() => props.name.toUpperCase())
</script>

<style lang="scss"></style>
