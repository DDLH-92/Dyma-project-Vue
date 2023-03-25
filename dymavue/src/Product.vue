<template>
  <h3>{{ title }}</h3>
</template>

<script lang="ts" setup>
import { computed } from 'vue'

const props = defineProps({
  name: {
    type: Object,
    default: 'Pomme'
  },
  prix: {
    type: Number,
    required: true
  }
})

const title = computed(() => props.name.toUpperCase())
</script>

<style lang="scss"></style>
