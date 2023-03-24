<template>
  <h1 v-memo="[title]"><p>{{ title }}</p></h1>
  <input type="text" v-model="input">
  <p>{{ input }}</p>
</template>

<script setup lang="ts">
import { ref } from 'vue'
const title = ref('Je suis un titre')
const input = ref('')
</script>
