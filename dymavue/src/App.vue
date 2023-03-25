<template>
  <button @click="toggle = !toggle">Toggle</button>
  <div v-if="toggle"><Blog />
  </div>

</template>

<script setup lang="ts">
import Blog from './Blog.vue'
import { ref } from 'vue'

const toggle = ref(true)

</script>
