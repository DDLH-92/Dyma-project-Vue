<template>
  <h2>Un titre d'article</h2>
  <button @click="$emit('bigger', 5)">+</button>
  <button @click="$emit('smaller', 5)">-</button>
  <p :style="{ fontSize: props.fontSize + 'px' }">Lorem ipsum dolor sit amet consectetur, adipisicing elit. Ex hic nostrum repellat? Sapiente quia iure ea asperiores non culpa iste impedit? Deserunt illo iure laudantium eos quo nam pariatur voluptate.</p>
</template>
<script lang="ts" setup>
import { defineProps } from 'vue';

const props = defineProps<{
  fontSize: number
}>()

const emit = defineEmits<{
  (e: 'bigger', inc: number): void
  (e: 'smaller'): void
}>()

</script>

<style lang="scss"></style>
